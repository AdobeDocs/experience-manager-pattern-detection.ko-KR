---
title: CTEM
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---


# CTEM {#ctem}

사용자 정의 템플릿

## 배경 {#background}

`CTEM` AEM에 설치된 사용자 정의 템플릿을 식별합니다. 이 정보는 모범 사례 평가를 위해 제공됩니다.

템플릿은 &quot;cq:Template&quot;의 기본 유형 값으로 식별됩니다. 템플릿 카테고리를 식별하기 위해 이 코드와 함께 하위 유형이 사용됩니다.

* `custom.editable.template`:템플릿의 경로는 &quot;/apps&quot;로 시작되지 않습니다.
* `custom.static.template`:템플릿의 경로는 &quot;/apps&quot;로 시작합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 가장 좋은 방법은 모든 정적 템플릿을 편집 가능한 템플릿으로 이동하는 것입니다.

## 가능한 솔루션 {#solutions}

* [AEM 현대화 도구](https://opensource.adobe.com/aem-modernize-tools/)를 활용하여 정적 템플릿을 편집 가능한 템플릿으로 마이그레이션합니다.
* 편집 가능한 템플릿에 대한 자세한 내용은 [템플릿](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html)에서 확인하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
