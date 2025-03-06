---
title: CIF
description: 패턴 감지기 코드 도움말 페이지.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 76%

---

# CIF {#cif}

Commerce Integration Framework 클래식

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework 클래식"
>abstract="CIF는 AEM as a Cloud Service와 호환되지 않는 클래식 버전의 Commerce Integration Framework 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content 및 Commerce"

`CIF`는 AEM as a Cloud Service와 호환되지 않는 클래식 버전의 Commerce Integration Framework 사용을 식별합니다. 각 `CIF` 결과에 대한 메시지는 사용을 식별하며 추가 정보를 제공합니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `commerce.integration.framework.detected`: 클래식 버전의 Commerce Integration Framework와 AEM as a Cloud Service의 비호환성


## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 모든 클래식 버전의 Commerce Integration Framework 사용을 검토하는 것입니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="CIF의 주요 변경 내용"

* 클래식 버전의 Commerce Integration Framework는 AEM as a Cloud Service에서 더 이상 지원되지 않습니다. AEM as a Cloud Service로의 업그레이드가 차단됩니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="도구 및 리소스"
>abstract="이 안내서를 통해 Experience Manager Cloud Service 마이그레이션을 위해 업데이트해야 하는 영역을 식별할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="CIF용 마이그레이션 안내서"

* Experience Manager as a Cloud Service의 경우, CIF 추가 기능은 Adobe Commerce 및 서드파티 상업 솔루션에 대해 유일하게 지원되는 상업 통합 솔루션입니다. Experience Manager as a Cloud Service의 고객에 대해 CIF 추가 기능이 자동으로 배포되므로 수동으로 배포하지 않아도 됩니다. [AEM Commerce as a Cloud Service 시작하기](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started)를 참조하십시오.
* Adobe는 CIF 배포 프로젝트를 지원하기 위해 [AEM CIF 핵심 구성 요소](https://github.com/adobe/aem-core-cif-components)를 제공합니다.
* [소프트웨어 배포 포털](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html)을 사용하여 AEM 6.5에서도 CIF 추가 기능을 사용할 수 있습니다. 이는 Experience Manager as a Cloud Service와 호환되며 Experience Manager as a Cloud Service용 CIF 추가 기능과 동일한 기능을 제공하므로 따로 조정하지 않아도 됩니다.
* 클래식 CIF와 그 종속성은 더 이상 사용할 수 없습니다. com.adobe.cq.commerce.api Java™ API를 사용하며 이 CIF 버전에 의존하는 코드는 CIF 추가 기능 및 그 원리에 맞춰 조정해야 합니다.

또한 아래에서 다양한 하위 유형에 대해 가능한 솔루션을 찾으십시오.

* `commerce.bundles.detected` - 업그레이드 중에 이 번들이 제거됩니다.
* `commerce.packages.detected` - 업그레이드 중에 이 패키지가 삭제됩니다.
* `commerce.packages.dependency` - 사용자 지정 패키지에서 Commerce에 대한 종속성을 제거합니다.
* `commerce.nodes.detected` - CQ Commerce 노드를 만들지 않도록 사용자 지정 코드를 업데이트합니다.
* `commerce.configs.detected` - 사용자 지정 코드에서 CQ Commerce 구성 속성을 사용하지 않음
* `commerce.users.detected` - 사용자 지정 코드에서 CQ Commerce 서비스 사용자를 사용하지 않음
* `commerce.overlays.detected` - CQ Commerce 오버레이 사용 제거
* `commerce.paths.detected` - 상거래 경로가 AEM에서 사용되고 있지 않은지 확인한 후 제거하십시오.
* `commerce.resource.type.detected` - 상거래 리소스 유형 사용 제거
* `commerce.usage` - 사용자 지정 코드에서 CQ Commerce API를 제거합니다.
