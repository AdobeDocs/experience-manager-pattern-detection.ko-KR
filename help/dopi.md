---
title: DOPI
description: 패턴 탐지기 코드 도움말 페이지
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# DOPI {#dopi}

사용되지 않는 순차적 속성 색인

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="사용되지 않는 순차적 속성 색인"
>abstract="DOPI 코드는 6.1 이후 사용되지 않고 6.2에서 제거되었던 순서가 지정된 속성 인덱스 정의(primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;)의 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="순서가 지정된 색인 - 사용되지 않음"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html" text="인덱싱 - AEM을 Cloud Service으로 사용"

`DOPI` 6.1 이후 사용되지 않고 6.2에서 제거되었던 순차적 속성 인덱스 정의(`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`)의 사용을 식별합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="구현 지침"
>abstract="우수 사례는 가치 없는 성능 문제나 비기능 고객 요구 사항을 피하기 위해 더 이상 사용되지 않는 모든 주문 인덱스를 검토하고 지원되는 유형의 루센 색인으로 이동하는 것입니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="우수 사례 - 쿼리 및 인덱싱"

* 일부 쿼리는 응답하지 않을 수 있습니다.
* 고객 기능이 제대로 작동하지 않을 수 있습니다.
* 더 이상 사용되지 않는 색인에는 영향을 주지 않으므로 트래픽 경고나 오류 및 심각한 성능 위반도 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 DOPI 위반이 AEM Cloud Service과 호환되는 방법을 파악하십시오. 또한 Github에서 DOPI 위반 예제를 검토하여 이전 순서가 지정된 인덱스를 AEM에서 Cloud Service으로 지원되는 Lucene 기반 인덱스로 변환하는 방법을 파악합니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="DOPI 위반 예 - Github"

* 인덱스 정의를 지원되는 색인 정의로 만들거나 바꿀 수 있습니다. ([Oak 쿼리 및 인덱싱](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html) 참조)
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) 프로젝트를 검토하고 [DOPI 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi)을 수정하여 Cloud Service과 호환되는 방법을 파악합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
