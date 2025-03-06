---
title: WRF
description: 패턴 감지기 코드 도움말 페이지.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# WRF {#wrf}

## 배경 {#background}

WRF는 AEM 6.5 LTS와 호환되지 않는 we-retail 사용을 식별합니다.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## 가능한 해결 방법 {#solutions}

아래에서 다양한 하위 유형에 대해 가능한 솔루션을 찾으십시오.

* `weretail.bundles.detected` - 업그레이드 중에 이 번들이 제거됩니다.
* `weretail.packages.detected` - 업그레이드 중에 이 패키지가 삭제됩니다.
* `weretail.configs.detected` - 사용자 지정 코드에서 We.Retail 구성 속성을 사용하지 않음
* `weretail.packages.dependency` - We.Retail에서 사용자 지정 패키지의 종속성을 제거합니다.
* `weretail.paths.detected` - 이 We.Retail 경로는 social을 사용하고 있지 않은지 확인한 후 삭제할 수 있습니다.
* `weretail.resource.type.detected` - We.Retail 리소스 유형 사용 제거
* `weretail.usage` - 사용자 지정 코드에서 We.Retail API를 제거합니다.