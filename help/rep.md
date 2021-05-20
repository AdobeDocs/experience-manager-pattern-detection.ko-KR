---
title: REP
description: 패턴 탐지기 코드 도움말 페이지
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 2%

---

# [!DNL REP] {#rep}

복제 에이전트

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="복제 에이전트"
>abstract="REP가 활성화된 복제 에이전트를 식별합니다. 이러한 보고서는 AEM을 Cloud Service으로 업그레이드할 때 해결해야 하는 문제가 발생할 수 있으므로 보고됩니다. AEM as a Cloud Service은 Sling 컨텐츠 배포 를 사용하여 작성자의 컨텐츠를 게시 환경에 배포합니다. 이 작업은 Adobe I/O의 파이프라인 서비스를 사용하여 AEM 런타임 외부에서 수행됩니다.프로비저닝된 AEM에서 Cloud Service 환경으로 자동으로 구성됩니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents" text="주요 변경 사항 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents" text="개발 지침"

`REP` 활성화된 복제 에이전트를 식별합니다. 이러한 보고서는 AEM을 Cloud Service으로 업그레이드할 때 해결해야 하는 문제가 발생할 수 있으므로 보고됩니다.

AEM as a Cloud Service은 [Sling 컨텐츠 배포](https://sling.apache.org/documentation/bundles/content-distribution.html)를 사용하여 작성자의 컨텐츠를 게시 환경에 배포합니다. 이 작업은 Adobe I/O의 파이프라인 서비스를 사용하여 AEM 런타임 외부에서 수행됩니다.프로비저닝된 AEM에서 Cloud Service 환경으로 자동으로 구성됩니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 복제 구성이 AEM as a Cloud Service으로 변경되었습니다. 모든 현재 복제 에이전트를 검토하여 표준 기능으로 대체되는 구성, 코드로 이동해야 하며 지원되지 않는 구성을 확인해야 합니다.
* AEM으로 Cloud Service으로 업그레이드하는 동안 사용자 지정 코드 또는 워크플로우에서 복제 에이전트를 사용하는 것은 검토해야 합니다.
* 역방향 복제는 처음에 AEM as a Cloud Service에서 지원되지 않습니다.
* 별도의 디스패처 플러시 에이전트를 구성할 필요가 없습니다. AEM에서 Cloud Service 환경으로 자동으로 구성됩니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="구현 지침"
>abstract="모범 사례는 복제 에이전트에 따라 직접 사용자 지정 기능을 검토, 리팩터링 및 최적화하고 AEM과 Cloud Service으로 호환되도록 하는 것입니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication" text="복제 - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* AEM as a Cloud Service [개발 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) 및 [복제 에이전트](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents)에 대한 릴리스 노트를 참조하십시오.
* 복제 에이전트에 따라 기능을 검토, 리팩터링 및 최적화하여 비즈니스 작업을 수행할 수 있습니다.
* [복제](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication)가 AEM에서 Cloud Service으로 배포의 영향을 받는 방식을 참조하십시오.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
