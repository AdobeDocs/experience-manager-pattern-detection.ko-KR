---
title: 교류
description: 패턴 감지기 코드 도움말 페이지.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# 교류 {#ac}

## 배경 {#background}

AC는 AEM 6.5 LTS와 호환되지 않는 Assets 번들 사용을 식별합니다

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## 가능한 해결 방법 {#solutions}

아래에서 다양한 하위 유형에 대해 가능한 솔루션을 찾으십시오.

* `asset.bundles.detected` - 업그레이드 중에 이 번들이 제거됩니다.
* `asset.usage` - 사용자 지정 코드에서 자산 등급 및 자산 카탈로그 구성 요소 종속성을 제거합니다. 해당하는 경우 새 API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`을(를) 사용하도록 코드를 변경하십시오.
* `asset.overlays.detected` - Assets 등급 및 카탈로그 구성 요소에서 만들어진 오버레이는 제거해야 합니다.
* `asset.resource.type.detected` - 사용자 지정 코드에서 Assets 등급 구성 요소 resourcetype 사용을 제거합니다.
* `asset.paths.detected` - AEM에서 사용되고 있지 않은지 확인한 후 이러한 경로 아래에 있는 고객 콘텐츠를 이동하고 이러한 경로를 제거합니다.