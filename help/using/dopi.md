---
title: DOPI
description: 패턴 감지기 코드 도움말 페이지.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 100%

---

# DOPI {#dopi}

더 이상 사용되지 않는 순서가 지정된 속성 색인

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="더 이상 사용되지 않는 순서가 지정된 속성 색인"
>abstract="DOPI 코드는 순서가 지정된 속성 색인 정의(`primaryType=oak:QueryIndexDefinition` 및 `type="ordered"`)의 사용을 식별합니다. 이 정의는 AEM 6.1에서 더 이상 사용되지 않으며, AEM 6.2에서 제거되었습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="순서가 지정된 색인 - 더 이상 사용되지 않는 기능"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/operations/indexing" text="색인화 - AEM as a Cloud Service"

`DOPI` 코드는 순서가 지정된 속성 색인 정의(`primaryType=oak:QueryIndexDefinition` 및 `type="ordered"`)의 사용을 식별합니다. 이 정의는 AEM 6.1에서 더 이상 사용되지 않으며, AEM 6.2에서 제거되었습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 더 이상 사용되지 않는 모든 순서가 지정된 색인을 검토한 다음 이를 지원되는 형식의 Lucene 색인으로 이동하여 심각한 성능 문제 또는 고객 요구 사항 관련 문제를 방지하는 것입니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="모범 사례 - 쿼리 및 색인화"

* 일부 쿼리가 응답하지 않을 수 있습니다.
* 고객 기능이 올바르게 작동하지 않을 수 있습니다.
* 더 이상 사용되지 않는 색인으로 인한 경고 또는 오류 및 심각한 성능 페널티는 영향을 주지 않습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 DOPI 위반이 AEM Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오. 또한 GitHub에서 DOPI 위반 사례를 검토하십시오. 이를 통해 순서가 지정된 기존의 색인을 AEM as a Cloud Service에서 지원되는 Lucene 기반 색인으로 변환할 수 있는 방법을 이해할 수 있습니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="WKND 레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="DOPI 위반 사례 - GitHub"

* 색인 정의를 지원되는 색인 정의가 되도록 편집하거나 지원되는 색인 정의로 대체하십시오. [Oak 쿼리 및 색인화](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing)를 참조하십시오.
* [WKND 레거시](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) 프로젝트를 검토한 다음 [DOPI 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi)을 수정하여 AEM as a Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
