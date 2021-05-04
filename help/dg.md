---
title: DG
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 1%

---

# DG {#dg}

개발자 지침

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="개발자 지침"
>abstract="DG 코드는 AEM 6.5 및 AEM에 대해 선택한 개발 지침을 Cloud Service으로 식별합니다. 다음 우수 사례를 통해 시스템의 유지 관리 능력과 성능을 향상시킬 수 있습니다. 이전 버전의 AEM을 포함하여 다른 응용 프로그램 컨텍스트에서는 이러한 편차 중 일부가 문제가 되지 않을 수 있지만 AEM을 Cloud Service으로 사용할 때 문제가 발생할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM 개발 - 지침 및 우수 사례"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="AEM as a Cloud Service 개발 지침"


`DG` AEM 6.5 및  [AEM에 대해 선택한 개발 지침](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) 의 편차를 Cloud Service으로 식별합니다 [ ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). 다음 우수 사례를 통해 시스템의 유지 관리 능력과 성능을 향상시킬 수 있습니다. 이전 버전의 AEM을 포함하여 다른 응용 프로그램 컨텍스트에서는 이러한 편차 중 일부가 문제가 되지 않을 수 있지만 AEM을 Cloud Service으로 사용할 때 문제가 발생할 수 있습니다.

하위 유형은 감지된 다양한 유형의 위반을 식별하는 데 사용됩니다.

* `java.io.inputstream`:응용 프로그램 코드 `java.io.InputStream` 에서 사용.
* `maintenance.task.configuration`:특정 정기 유지 관리 활동의 구성.
* `sling.commons.scheduler`:예약된 작업에 Sling Commons Scheduler API를 사용합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* `java.io.inputstream`
   * `java.io.InputStream`이(가) 있는 이진 데이터의 스트리밍은 성능에 영향을 주는 지점까지 메모리 리소스를 사용할 수 있습니다. 특히 Cloud Service으로 AEM에 사용되는 컨테이너에서 사용할 수 있는 메모리가 제한되어 있는 문제가 발생합니다.

* `maintenance.task.configuration`
   * 이전에 명시적 구성이 필요한 일부 유지 관리 작업은 이제 Cloud Service으로 AEM 내에서 자동으로 구성되고 관리됩니다.
   * Cloud Service의 유지 관리 작업 구성을 소스 제어로 이동해야 합니다.

* `sling.commons.scheduler`
   * [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html)를 사용하는 백그라운드 작업에 종속된 응용 프로그램은 AEM에서 Cloud Service으로 실행을 보장할 수 없으므로 예상대로 작동하지 않을 수 있습니다.
   * AEM은 [백그라운드 작업과 긴 실행 작업](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs)에 대한 Cloud Service 개발 지침으로서 예약된 작업으로 실행되는 코드가 실행 중인 인스턴스를 언제든지 중지할 수 있다고 가정해야 합니다. 따라서 코드는 복원력이 있고 다시 시작할 수 있어야 합니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="구현 지침"
>abstract="AEM 개발 지침 및 모범 사례에 따라 고객은 Sling Commons Scheduler 사용에 대한 구현을 검토하고 Sling Jobs로 재구성하여 시스템 유지 관리 작업을 다시 구성하고 바이너리 데이터의 스트리밍을 검토하고 코드를 Cloud Service으로 AEM과 호환되도록 재평가해야 합니다."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling 작업"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html" text="Cloud Service의 유지 관리 작업"

* `java.io.inputstream`
   * 바이너리가 데이터 저장소에 직접 추가되는 직접적인 바이너리 업로드 방법을 사용합니다.
   * 자산 사용 사례의 경우 [aem-upload](https://github.com/adobe/aem-upload)를 사용하십시오. 다른 유형의 바이너리의 경우 동일한 패턴을 기준으로 사용자 지정 업로드 논리를 모델링할 수 있습니다.

* `maintenance.task.configuration`
   * AEM을 Cloud Service [유지 관리 작업](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html) 설명서로 검토합니다.
   * [유지 관리 작업 구성](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control)이(가) 소스 제어에 있는지 확인합니다.

* `sling.commons.scheduler`
   * [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html)를 [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing)로 대체하여 한 번 이상 실행 보증을 제공합니다.
   * 가능하면 장시간 실행되는 작업은 피해야 한다.

* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
