---
title: SCR
description: 패턴 감지기 코드 도움말 페이지.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# SCR {#scr}

## 배경 {#background}

SIF는 AEM 6.5 LTS와 호환되지 않는 AEM Screens 사용을 식별합니다.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## 가능한 해결 방법 {#solutions}

아래에서 다양한 하위 유형에 대해 가능한 솔루션을 찾으십시오.

* `screens.bundles.detected` - 업그레이드 중에 이러한 번들이 제거됩니다.
* `screens.packages.detected` - 업그레이드 중에 이 패키지가 삭제됩니다.
* `screens.packages.dependency` - 사용자 지정 패키지에서 Screens에 대한 종속성을 제거합니다.
* `screens.configs.detected` - 사용자 지정 코드에서 Screens 구성 속성을 사용하고 있지 않은지 확인하십시오.
* `screens.users.detected` - 사용자 지정 코드에서 Screens 서비스 사용자를 사용하고 있지 않은지 확인하십시오.
* `screens.paths.detected` - Screens 경로가 AEM에서 사용되고 있지 않은지 확인한 후 제거하십시오.
* `screens.resource.type.detected` - Screens 리소스 유형 사용을 제거합니다.
* `screens.usage` - 사용자 지정 코드에서 Screens API를 제거합니다.