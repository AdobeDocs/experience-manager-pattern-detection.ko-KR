---
title: DOPI
description: 패턴 탐지기 코드 도움말 페이지
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# DOPI {#dopi}

사용되지 않는 순서가 지정된 속성 인덱스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="사용되지 않는 순서가 지정된 속성 인덱스"
>abstract="DOPI 코드는 6.1 이후 더 이상 사용되지 않고 6.2에서 제거된 순서가 지정된 속성 인덱스 정의(primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;)의 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="순서가 지정된 색인 - 사용되지 않음"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html" text="색인 지정 - AEM as a Cloud Service"

`DOPI` 6.1 이후 사용이 중단되었으며 6.2에서 제거된 순서가 지정된 속성 색인 정의(`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`)의 사용을 식별합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="구현 지침"
>abstract="모범 사례는 사용되지 않는 모든 순차 인덱스를 검토하고 지원되는 형식의 lucene 인덱스로 이동하여 중요한 성능 문제나 비기능 고객 요구 사항을 방지하는 것입니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="우수 사례 - 쿼리 및 색인 지정"

* 일부 쿼리는 응답하지 않을 수 있습니다.
* 고객 기능이 제대로 작동하지 않을 수 있습니다.
* 사용되지 않는 인덱스는 영향을 주지 않으므로 순회 경고 또는 오류와 상당한 성능 위반이 발생합니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="도구 및 리소스"
>abstract="WKND-legacy 프로젝트를 검토하여 DOPI 위반을 AEM Cloud Service과 호환하는 방법을 이해합니다. 또한 Github의 DOPI 위반 예제를 검토하여 순서가 지정된 레거시 인덱스가 AEM에서 Cloud Service으로 지원되는 Lucene 기반 인덱스로 변환되는 방법을 이해합니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND-이전 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="DOPI 위반 예 - Github"

* 인덱스 정의를 지원되는 인덱스 정의로 만들거나 바꿀 수 있습니다. ([Oak 쿼리 및 색인 지정](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html) 참조).
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) 프로젝트를 검토하고 [DOPI 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi)을 수정하고 Cloud Service으로 AEM과 호환되는 방법을 이해합니다.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
