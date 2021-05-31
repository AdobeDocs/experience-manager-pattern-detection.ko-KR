---
title: CIF
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84aea5b24e51ce5672826bad4ec126074bf24a09
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
>abstract="CIF는 AEM과 Cloud Service으로 호환되지 않는 클래식 버전의 Commerce Integration Framework 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" 콘텐츠 및 상거래"

`CIF` CIF는 AEM과 Cloud Service으로 호환되지 않는 클래식 버전의 Commerce Integration Framework 사용을 식별합니다. 각 `CIF` 검색 결과에 대한 메시지는 사용량을 식별하고 추가 정보를 제공합니다.

하위 유형은 다양한 유형의 정보를 식별하는 데 사용됩니다.

* `commerce.integration.framework.detected`:Commerce Integration Framework의 클래식 버전과 AEM as a Cloud Service이 호환하지 않습니다.


## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="구현 지침"
>abstract="모범 사례는 모든 클래식 버전의 Commerce Integration Framework 사용을 검토하는 것입니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="CIF에 대한 주요 변경 사항"

* Commerce Integration Framework의 클래식 버전은 더 이상 AEM에서 Cloud Service으로 지원되지 않습니다. Cloud Service으로 AEM로의 업그레이드를 차단합니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="도구 및 리소스"
>abstract="이 안내서는 Experience Manager Cloud Service 마이그레이션을 위해 업데이트해야 하는 영역을 식별하는 데 도움이 됩니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="CIF용 마이그레이션 안내서"

* Cloud Service의 경우 CIF 추가 기능은 Adobe 상거래 및 타사 상거래 솔루션에 대해 지원되는 유일한 상거래 통합 솔루션입니다. CIF 추가 기능은 Cloud Service으로 Experience Manager에 있는 고객을 위해 자동으로 배포되므로 수동 배포가 필요하지 않습니다. [Cloud Service으로 AEM Commerce 시작하기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html)를 참조하십시오.
* CIF Adobe 배포를 지원하는 프로젝트에서는 [AEM CIF 코어 구성 요소](https://github.com/adobe/aem-core-cif-components)를 제공합니다.
* CIF 추가 기능은 [소프트웨어 배포 포털](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html)을 통해서도 AEM 6.5에 사용할 수 있습니다. 호환되며 Cloud Service으로 Experience Manager에 대한 CIF 추가 기능과 동일한 기능을 제공합니다. 조정할 필요가 없습니다.
* 종속성이 있는 클래식 CIF는 더 이상 사용할 수 없습니다. com.adobe.cq.commerce.api Java API를 사용하여 이 CIF 버전에 의존하는 코드는 CIF 추가 기능 및 해당 원칙에 따라 조정해야 합니다.
