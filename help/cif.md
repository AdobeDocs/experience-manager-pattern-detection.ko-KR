---
title: CIF
description: 패턴 탐지기 코드 도움말 페이지
source-git-commit: b611b595267e60df8a15511a8a2b4b30b601df1b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---

# CIF {#cif}

Commerce Integration Framework Classic

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF는 AEM as a Cloud Service과 호환되지 않는 Commerce Integration Framework 사용의 클래식 버전을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" 콘텐츠 및 상거래"

`CIF` CIF는 AEM as a Cloud Service과 호환되지 않는 Commerce Integration Framework 사용의 클래식 버전을 식별합니다. 각 `CIF` 검색 결과는 사용량을 식별하고 추가 정보를 제공합니다.

하위 유형은 다양한 유형의 정보를 식별하는 데 사용됩니다.

* `commerce.integration.framework.detected`: Commerce Integration Framework의 클래식 버전과 AEM as a Cloud Service이 호환되지 않습니다.


## 가능한 의미와 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="구현 지침"
>abstract="모범 사례는 모든 클래식 버전의 Commerce Integration Framework 사용을 검토하는 것입니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="CIF에 대한 주요 변경 사항"

* Commerce Integration Framework의 클래식 버전은 더 이상 AEM as a Cloud Service에서 지원되지 않습니다. AEM as a Cloud Service로의 업그레이드를 차단합니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="도구 및 리소스"
>abstract="이 안내서는 Experience Manager Cloud Service 마이그레이션을 위해 업데이트해야 하는 영역을 식별하는 데 도움이 됩니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="CIF용 마이그레이션 안내서"

* Experience Manager의 경우 as a Cloud Service CIF 추가 기능은 Adobe Commerce 및 타사 상거래 솔루션에 대해 지원되는 유일한 상거래 통합 솔루션입니다. CIF 추가 기능은 Experience Manager as a Cloud Service에서 고객을 위해 자동으로 배포되므로 수동 배포가 필요하지 않습니다. 자세한 내용은 [AEM Commerce as a Cloud Service 시작하기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* CIF Adobe 배포 프로젝트를 지원하기 위해 다음을 제공합니다. [AEM CIF 코어 구성 요소](https://github.com/adobe/aem-core-cif-components).
* CIF 추가 기능은 AEM 6.5뿐만 아니라 [소프트웨어 배포 포털](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). 호환되며 Experience Manager as a Cloud Service용 CIF 추가 기능과 동일한 기능을 제공합니다. 조정 필요 없습니다.
* 종속성이 있는 클래식 CIF는 더 이상 사용할 수 없습니다. com.adobe.cq.commerce.api Java API를 사용하여 이 CIF 버전에 의존하는 코드는 CIF 추가 기능 및 해당 원칙에 따라 조정해야 합니다.
