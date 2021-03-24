---
title: REP
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---


# [!DNL REP] {#rep}

복제 에이전트

## 배경 {#background}

`REP` 활성화된 복제 에이전트를 식별합니다. 이러한 문제는 Cloud Service으로 AEM으로 업그레이드할 때 해결해야 하는 문제가 발생할 수 있기 때문에 보고됩니다.

AEM은 [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html)을 사용하여 작성자의 컨텐츠를 게시 환경으로 배포합니다. Adobe I/O의 파이프라인 서비스를 사용하여 AEM 런타임 외부에서 수행됩니다.제공된 AEM에서 Cloud Service 환경으로 자동으로 구성됩니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 복제 구성이 AEM에서 Cloud Service으로 변경되었습니다. 현재 모든 복제 에이전트를 검토하여 표준 기능으로 대체되는 구성, 코드로 이동해야 하는 구성 및 지원되지 않는 구성을 확인해야 합니다.
* 사용자 지정 코드 또는 워크플로우에서 복제 에이전트를 Cloud Service으로 업그레이드하는 동안 검토해야 합니다.
* 역방향 복제는 처음에 AEM에서 Cloud Service으로 지원되지 않습니다.
* 별도의 디스패처 플러시 에이전트를 구성할 필요가 없습니다. AEM에서 Cloud Service 환경으로 자동으로 구성됩니다.

## 가능한 솔루션 {#solutions}

* AEM을 Cloud Service [개발 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) 및 [복제 에이전트](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents)에 대한 릴리스 노트를 참조하십시오.
* 복제 에이전트에 따라 기능을 직접 검토, 리팩터 및 최적화하여 비즈니스 작업을 수행합니다.
* [복제](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication)가 Cloud Service으로 AEM에서 배포의 영향을 받는 방식을 참조하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
