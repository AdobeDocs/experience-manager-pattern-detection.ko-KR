---
title: DOPI
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

사용되지 않는 순차적 속성 색인

## 배경 {#background}

`DOPI` 6.1 이후 사용되지 않고 6.2에서 제거되었던 순차적 속성 인덱스 정의(`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`)의 사용을 식별합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 일부 쿼리는 응답하지 않을 수 있습니다.
* 고객 기능이 제대로 작동하지 않을 수 있습니다.
* 더 이상 사용되지 않는 색인에는 영향을 주지 않으므로 트래픽 경고나 오류 및 심각한 성능 위반도 있습니다.

## 가능한 솔루션 {#solutions}

* 인덱스 정의를 지원되는 색인 정의로 만들거나 바꿀 수 있습니다. ([Oak 쿼리 및 인덱싱](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html) 참조)
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) 프로젝트를 검토하고 [DOPI 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi)을 수정하여 Cloud Service과 호환되는 방법을 파악합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
