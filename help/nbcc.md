---
title: NBCC
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# NBCC {#nbcc}

역호환하지 않는 변경 사항

## 배경 {#background}

`NBCC` 호환되지 않는 방식으로 일부 JCR 노드 또는 번들이 변경되는 상황을 식별합니다. 고객은 업그레이드 전에 이러한 변경 사항을 알지 못할 수 있습니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 하위 호환되지 않는 변경 사항을 사용하는 구성 요소에 의존하는 기능은 끊길 수 있으며 올바로 확인되지 않을 수 있습니다.
* 고객 응용 프로그램의 일부 기능 또는 일부 AEM 기능이 업그레이드 후 제대로 작동하지 않을 수 있습니다.

## 가능한 솔루션 {#solutions}

* 이전 버전과 호환되는 Sling 구성 요소만 오버레이 또는 참조합니다.
* AEM 업그레이드 후 `/libs` 또는 번들에서 제공하는 리소스를 다시 적용하는 것을 고려해 보십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
