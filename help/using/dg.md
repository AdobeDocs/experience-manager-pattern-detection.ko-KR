---
title: DG
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 90%

---

# DG {#dg}

개발자 가이드라인

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="개발자 가이드라인"
>abstract="DG 코드는 선택된 AEM 6.5 및 AEM as a Cloud Service용 개발 지침의 위반을 식별합니다. 다음 모범 사례를 통해 시스템의 유지 가능성 및 성능을 개선할 수 있습니다. 이들 위반 중 일부는 이전 버전의 AEM을 포함하여 다른 애플리케이션 컨텍스트에서는 문제가 되지 않을 수 있지만, AEM as a Cloud Service와 함께 사용할 경우에는 문제를 발생시킬 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM 개발 - 지침 및 우수 사례"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="AEM as a Cloud Service 개발 지침"


`DG`는 선택된 [AEM 6.5](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) 및 [AEM as a Cloud Service](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines)용 개발 지침의 위반을 식별합니다. 다음 모범 사례를 통해 시스템의 유지 가능성 및 성능을 개선할 수 있습니다. 이들 위반 중 일부는 이전 버전의 AEM을 포함하여 다른 애플리케이션 컨텍스트에서는 문제가 되지 않을 수 있지만, AEM as a Cloud Service와 함께 사용할 경우에는 문제를 발생시킬 수 있습니다.

다양한 유형의 감지된 위반을 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `java.io.inputstream`: 애플리케이션 코드의 `java.io.InputStream` 사용
* `maintenance.task.configuration`: 특정 정기 유지 관리 활동 구성
* `sling.commons.scheduler`: 예정된 작업에 대한 Sling Commons 스케줄러 API 사용
* `unsupported.asset.api`: 애플리케이션 코드에서 지원되지 않는 자산 관리자 API 사용
* `javax.jcr.observation.EventListener`: 애플리케이션 코드에서 이벤트 리스너 사용
* `custom.guava.cache`: 애플리케이션 코드에서 Guava 캐시 사용

## 가능한 영향 및 위험 {#implications-and-risks}

* `java.io.inputstream`
   * `java.io.InputStream`이 있는 바이너리 데이터를 스트리밍하면 성능에 영향을 줄 만큼의 메모리 리소스를 사용합니다. 이 문제는 AEM에서 as a Cloud Service으로 사용되는 컨테이너에서 사용할 수 있는 메모리가 제한적이기 때문입니다.

* `maintenance.task.configuration`
   * 이전에는 명시적 구성이 필요했던 일부 유지 관리 작업은 이제 AEM as a Cloud Service에서 자동으로 구성 및 관리됩니다.
   * AEM as a Cloud Service에서의 유지 관리 작업 구성은 소스 제어로 이동해야 합니다.

* `sling.commons.scheduler`
   * [Sling Commons 스케줄러](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html)를 사용하는 배경 작업에 종속된 애플리케이션은 AEM as a Cloud Service에서의 실행이 보장되지 않으므로 예상대로 작동하지 않을 수 있습니다.
   * [배경 작업 및 장기 실행 작업](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs)을 위한 지침은 예정된 작업으로 실행된 코드는 해당 코드에서 실행 중인 인스턴스가 언제든지 중단될 가능성이 있음을 가정해야 한다고 제안합니다. 따라서 해당 코드는 탄력적이고 복원 가능한 상태여야 합니다.

* `unsupported.asset.api`
   * AssetManager의 다음 API는 AEM as a Cloud Service에서 지원되지 않는 것으로 표시됩니다.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * 실행을 보장할 수 없기 때문에 이벤트 리스너에 종속된 응용 프로그램이 예상대로 작동하지 않을 수 있습니다.

* `custom.guava.cache`
   * Guava 캐시를 사용하면 AEM에서 성능 문제가 발생할 수 있습니다.


## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="구현 지침"
>abstract="Sling Commons 스케줄러 사용에 대한 구현을 검토하십시오. Sling 작업으로 재구성하고, 시스템 유지 관리 작업을 재구성하고, 이진 데이터의 스트리밍을 검토하고, AEM as a Cloud Service를 준수하도록 코드를 리팩터링합니다."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Sling 작업"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/operations/maintenance" text="AEM as a Cloud Service에서의 유지 관리 작업"

* `java.io.inputstream`
   * 데이터 스토어에 바이너리를 바로 추가하는 다이렉트 바이너리 업로드 방식을 사용하십시오.
   * 자산 사용 사례의 경우 [AEM 업로드](https://github.com/adobe/aem-upload)를 참조하십시오. 다른 바이너리 유형의 경우 동일한 패턴을 따라 사용자 정의 업로드 논리를 모델링할 수 있습니다.

* `maintenance.task.configuration`
   * AEM as a Cloud Service [유지 관리 작업](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/operations/maintenance) 설명서를 검토하십시오.
   * [유지 관리 작업 구성](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control)은 소스 제어에 배치되어야 합니다.

* `sling.commons.scheduler`
   * [Sling Commons 스케줄러](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) 사용을 최소 한 번 이상의 실행이 보장된 [Sling 작업](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing)으로 대체하십시오.
   * 장기 실행 작업을 피하십시오.

* `unsupported.asset.api`
   * 자산 관리자의 지원되지 않는 API를 사용하지 말고 [AEM 업로드](https://github.com/adobe/aem-upload)를 참조하십시오.

* `javax.jcr.observation.EventListener`
   * 이벤트 리스너를 사용하는 대신 처리 보장을 제공하므로 이벤트 처리 메커니즘을 [Sling 작업](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing)으로 리팩터링하는 것이 좋습니다.

* `custom.guava.cache`
   * 필요한 경우, 캐시는 AEM 외부에서 생성되어야 합니다. 외부 캐싱 솔루션을 고려해 볼 수 있습니다.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
