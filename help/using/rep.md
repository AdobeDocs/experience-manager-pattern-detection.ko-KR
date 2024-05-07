---
title: REP
description: 패턴 감지기 코드 도움말 페이지.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '414'
ht-degree: 100%

---

# [!DNL REP] {#rep}

복제 에이전트

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="복제 에이전트"
>abstract="REP는 활성화된 복제 에이전트를 식별합니다. 이들 에이전트는 AEM as a Cloud Service로 업그레이드할 때 해결해야 할 문제의 발생 가능성을 감지하기 위해 보고됩니다. AEM as a Cloud Service는 Sling 콘텐츠 배포를 사용하여 작성자 환경에서 게시 환경으로 콘텐츠를 배포합니다. 이는 Adobe Developer에서 Adobe I/O Runtime의 파이프라인 서비스를 사용하여 AEM 런타임 외부에서 수행됩니다. 이는 프로비저닝된 AEM as a Cloud Service 환경에 자동으로 구성됩니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="개발 지침"

`REP`는 활성화된 복제 에이전트를 식별합니다. 이들 에이전트는 AEM as a Cloud Service로 업그레이드할 때 해결해야 할 문제의 발생 가능성을 감지하기 위해 보고됩니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `forward.replication`: 활성화된 순방향 복제 에이전트를 식별합니다.
* `reverse.replication`: 활성화된 역방향 복제 에이전트를 식별합니다.
* `standard.replication.agent.modification`: 활성화되고 수정되는 표준 복제 에이전트를 식별합니다.
* `custom.replication.agent.detection`: 활성화된 사용자 정의 복제 에이전트를 식별합니다.

AEM as a Cloud Service는 [Sling 콘텐츠 배포](https://sling.apache.org/documentation/bundles/content-distribution.html)를 사용하여 작성자 환경에서 게시 환경으로 콘텐츠를 배포합니다. 이는 Adobe Developer에서 Adobe I/O Runtime의 파이프라인 서비스를 사용하여 AEM 런타임 외부에서 수행됩니다. 이는 프로비저닝된 AEM as a Cloud Service 환경에 자동으로 구성됩니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* AEM as a Cloud Service와 함께 복제 구성이 변경되었습니다. 모든 현재 복제 에이전트를 검토하여 표준 기능으로 대체된 기능은 무엇인지, 코드로 이동해야 하는 구성은 무엇인지, 지원되지 않는 기능은 무엇인지 확인해야 합니다.
* AEM as a Cloud Service로 업그레이드 시 사용자 정의 코드 또는 워크플로에서의 복제 에이전트 사용을 검토해야 합니다.
* 복제 되돌리기 기능은 AEM as a Cloud Service에서 지원되지 않습니다.
* 개별 Dispatcher 플러시 에이전트를 구성하지 않아도 됩니다. 이는 AEM as a Cloud Service 환경에 자동으로 구성됩니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 복제 에이전트에 전적으로 의존하는 맞춤형 기능을 검토하고, 리팩터링하고, 최적화하여 AEM as a Cloud Service와 호환되도록 하는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="복제 - AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* AEM as a Cloud Service [개발 지침](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) 및 [복제 에이전트](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents)용 릴리스 정보를 참조하십시오.
* 비즈니스 작업 수행을 위해 복제 에이전트에 전적으로 의존하는 기능을 검토하고, 리팩터링하십시오.
* [복제](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication)가 어떻게 AEM as a Cloud Service에서 배포의 영향을 받는지 알아보십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
