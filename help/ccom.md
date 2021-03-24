---
title: CCOM
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# CCOM {#ccom}

사용자 지정 구성 요소

## 배경 {#background}

`CCOM` AEM에 설치된 사용자 지정 구성 요소를 식별합니다. 이 정보는 모범 사례 평가를 위해 제공됩니다.

하위 유형은 구성 요소의 카테고리를 식별하기 위해 이 코드와 함께 사용됩니다.

* `custom.core`:구성 요소의 수퍼 유형 체인에 있는 수퍼 유형에는 핵심 구성 요소에서 상속됨을 나타내는 &quot;core/wcm/components/&quot;가 포함되어 있습니다.
* `custom.foundation`:구성 요소의 수퍼 유형 체인에 있는 수퍼 유형에는 핵심 구성 요소에서 상속됨을 나타내는 &quot;core/wcm/components/&quot;가 포함되어 있습니다.
* `custom.overlay.foundation`:구성 요소 경로에는 기본 구성 요소를 오버레이하고 있음을 나타내는 &quot;wcm/foundation/components/&quot; 또는 &quot;foundation/components/&quot;가 포함되어 있습니다.
* `custom`:사용자 지정 구성 요소는 핵심 또는 기본 구성 요소를 상속하거나 오버레이하지 않습니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 우수 사례는 맞춤형 구성 요소 수를 최소화하고 핵심 구성 요소를 활용하고 스타일 시스템과 함께 핵심 구성 요소를 사용하여 기술 부채를 줄이는 것입니다.

## 가능한 솔루션 {#solutions}

* 핵심 구성 요소에 대한 자세한 내용은 [핵심 구성 요소 소개](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html)에서 확인하십시오.
* 스타일 시스템에 대한 자세한 내용은 [스타일 시스템 사용](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring)에서 확인하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
