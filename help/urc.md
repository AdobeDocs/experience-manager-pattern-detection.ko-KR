---
title: URC
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

지원되지 않는 런타임 모드 구성

## 배경 {#background}

`URC` 은 AEM에서 지원되지 않는 런타임 모드 이름을 기반으로 한 구성을 Cloud Service으로 식별합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* Cloud Service으로 AEM의 런타임 모드에 사용할 수 있는 이름 집합이 제한됩니다.
* 지원되지 않는 런타임 모드 이름을 기반으로 하는 구성은 Cloud Service으로 AEM에 배포될 때 아무런 효과가 없습니다.

## 가능한 솔루션 {#solutions}

* 이 구성을 검토하여 필요한 경우 확인합니다.
* 지원되는 [runmode names](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) 중 하나를 사용하도록 구성 이름을 변경하고 [runmode 해상도 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution)을 따릅니다.
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) 프로젝트를 검토하고 [URC 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc)을 수정하여 Cloud Service과 호환되는 방법을 파악합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
