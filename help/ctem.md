---
title: CTEM
description: 패턴 탐지기 코드 도움말 페이지
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 5%

---

# CTEM {#ctem}

사용자 정의 템플릿

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="사용자 정의 템플릿"
>abstract="CTEM은 AEM에 설치된 사용자 지정 구성 요소를 식별합니다. 이 정보는 모범 사례 평가를 위해 제공됩니다."

`CTEM` AEM에 설치된 사용자 정의 템플릿을 식별합니다. 이 정보는 모범 사례 평가를 위해 제공됩니다.

템플릿은 &quot;cq:Template&quot;의 기본 유형 값으로 식별됩니다. 템플릿 카테고리를 식별하기 위해 이 코드와 함께 하위 유형이 사용됩니다.

* `custom.editable.template`:템플릿의 경로는 &quot;/apps&quot;로 시작되지 않습니다.
* `custom.static.template`:템플릿의 경로는 &quot;/apps&quot;로 시작합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 모든 정적 템플릿을 편집 가능한 템플릿으로 이동하는 것입니다. 고객은 기존 AEM 현대화 도구를 사용하여 정적 템플릿을 편집 가능한 템플릿으로 마이그레이션할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html" text="편집 가능한 템플릿"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM 현대화 도구"

* 가장 좋은 방법은 모든 정적 템플릿을 편집 가능한 템플릿으로 이동하는 것입니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="도구 및 리소스"
>abstract="AEM Modern Suite의 도움으로 고객은 정적 정의에서 편집 가능한 템플릿으로 페이지의 구조를 수정할 수 있습니다. 고객이 기존 기능의 제한된 기능에서 강력하고 최신 AEM 서비스로 전환할 수 있도록 지원하기 위한 것입니다. 이러한 도구는 구성 인식 및 확장 가능한 구성 도구입니다. 도움말 및 분류에 대한 Adobe 지원"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="페이지 구조 변환기"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* [AEM 현대화 도구](https://opensource.adobe.com/aem-modernize-tools/)를 활용하여 정적 템플릿을 편집 가능한 템플릿으로 마이그레이션합니다.
* 편집 가능한 템플릿에 대한 자세한 내용은 [템플릿](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html)에서 확인하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
