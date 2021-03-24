---
title: OCU
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

오래된 코드 사용

## 배경 {#background}

`OCU` Sling 또는 AEM 구성 요소나 API OSGi 내보내기 등 일부 JCR 노드가 호환되지 않는 방식으로 변경되거나 제거되는 상황을 식별합니다. 고객은 업그레이드 전에 이러한 변경 사항을 알지 못할 수 있습니다. 호환되지 않는 버전으로 업그레이드하거나 전혀 사용할 수 없을 수 있습니다.

이전 버전이 기본적으로 설치되지 않았으므로 고객 응용 프로그램이 제대로 작동하지 않을 수 있습니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 더 이상 사용되지 않는 구성 요소 또는 API를 사용하는 구성 요소에 의존하는 기능은 중단될 수 있으며 업그레이드 후 올바르게 확인되지 않을 수 있습니다.
* 고객 응용 프로그램의 일부 기능 또는 일부 AEM 기능이 제대로 작동하지 않거나 업그레이드 후 활성 상태가 아닐 수 있습니다.

## 가능한 솔루션 {#solutions}

* 단기:호환성 패키지를 설치하는 데 도움이 될 수 있습니다.
* 장기:최신 버전의 AEM 구성 요소 또는 API를 사용하도록 고객 코드를 조정할 수 있습니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
