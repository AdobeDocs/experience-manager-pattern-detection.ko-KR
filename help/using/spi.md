---
title: SPI
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 39f2d04e-c6e4-4da6-b000-0115bc2b87bf
source-git-commit: 29d702c9662fd185ef806123fc4f4a03a70d64aa
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# SPI {#spi}

## 배경 {#background}

SIF는 AEM 6.5 LTS와 호환되지 않는 Search and Promote 사용을 식별합니다.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## 가능한 해결 방법 {#solutions}

아래에서 다양한 하위 유형에 대해 가능한 솔루션을 찾으십시오.

* `searchpromote.bundles.detected` - 업그레이드 중에 이러한 번들이 제거됩니다.
* `earchpromote.packages.detected` - 업그레이드 중에 이 패키지가 삭제됩니다.
* `searchpromote.packages.dependency` - 사용자 지정 패키지에 있는 검색 및 승격 종속성을 제거합니다.
* `searchpromote.usage` - 사용자 지정 코드에서 Search &amp; Promote API 제거
* `searchpromote.users.detected` - 사용자 지정 코드에서 Search &amp; Promote 서비스 사용자를 사용하지 않음
* `searchpromote.configs.detected` - 사용자 지정 코드에서 Search &amp; Promote 구성 속성을 사용하지 않습니다.
