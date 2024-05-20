---
title: CTEM
description: 패턴 감지기 코드 도움말 페이지.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 71%

---

# CTEM {#ctem}

사용자 정의 템플릿

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="사용자 정의 템플릿"
>abstract="CTEM은 AEM에 설치된 사용자 지정 구성 요소를 식별합니다. 이 정보는 모범 사례 평가 목적으로 제공됩니다."

`CTEM`  AEM에 설치된 사용자 지정 템플릿을 식별합니다. 이 정보는 모범 사례 평가 목적으로 제공됩니다.

템플릿의 기본 유형 값은 다음과 같습니다. `cq:Template`: 식별에 도움이 됩니다. 템플릿의 범주를 식별하기 위해 하위 유형이 이 코드와 함께 사용됩니다.

* `custom.editable.template`: 템플릿 경로가 다음으로 시작하지 않음 `/apps`.
* `custom.static.template`: 다음으로 시작하는 템플릿 경로 `/apps`.

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 모든 정적 템플릿을 편집 가능한 템플릿으로 이동하는 것입니다. 고객은 기존 AEM 현대화 도구를 통해 정적 템플릿을 편집 가능한 템플릿으로 마이그레이션할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="편집 가능한 템플릿"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM 현대화 도구"

* 가장 좋은 방법은 모든 정적 템플릿을 편집 가능한 템플릿으로 이동하는 것입니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="도구 및 리소스"
>abstract="AEM 현대화 제품군을 통해 고객은 정적 정의에서 편집 가능한 템플릿으로 페이지 구조를 조작할 수 있습니다. 이는 고객이 제한된 기존 기능에서 강력한 최신 AEM 서비스로 전환하는 것을 돕기 위함입니다. 이들 기능은 구성, 구성 인식 및 확장이 가능합니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="페이지 구조 변환기"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* [AEM 현대화 도구](https://opensource.adobe.com/aem-modernize-tools/)를 사용하여 정적 템플릿을 편집 가능한 템플릿으로 마이그레이션할 수 있습니다.
* [템플릿](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/platform/templates/templates)에서 편집 가능한 템플릿에 대해 자세히 알아보십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
