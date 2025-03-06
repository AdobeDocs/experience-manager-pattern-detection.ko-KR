---
title: SIF
description: 패턴 감지기 코드 도움말 페이지.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# SIF {#sif}

## 배경 {#background}

SIF는 AEM 6.5 LTS와 호환되지 않는 Social 사용을 식별합니다.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## 가능한 해결 방법 {#solutions}

아래에서 다양한 하위 유형에 대해 가능한 솔루션을 찾으십시오.

* `social.bundles.detected` - 업그레이드 중에 이 번들이 제거됩니다.
* `social.packages.detected` - 업그레이드 중에 이 패키지가 삭제됩니다.
* `social.packages.dependency` - 사용자 지정 패키지에서 Social의 패키지 종속성을 제거하십시오.
* `social.nodes.detected` - 소셜 노드를 만들지 않도록 사용자 지정 코드 업데이트
* `social.configs.detected` - 사용자 지정 코드에서 소셜 구성 속성을 사용하지 않음
* `social.users.detected` - 사용자 지정 코드에서 소셜 사용자 사용 안 함
* `social.overlays.detected` - 소셜 오버레이 사용 제거
* `social.paths.detected` - 소셜 경로가 AEM에서 사용되고 있지 않은지 확인한 후 제거하십시오.
* `social.resource.type.detected` - 소셜 리소스 유형 사용 제거
* `social.usage` - 사용자 지정 코드에서 소셜 API를 제거합니다.