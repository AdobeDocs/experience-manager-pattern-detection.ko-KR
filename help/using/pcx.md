---
title: PCX
description: 패턴 감지기 코드 도움말 페이지
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 100%

---

# PCX {#pcx}

페이지 복잡성

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="페이지 복잡성"
>abstract="PCX는 구조에 대량의 노드가 포함된 페이지를 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=ko-kr" text="AEM as a Cloud Service - 릴리스 정보"

`PCX`는 구조에 대량의 노드가 포함된 페이지를 식별합니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `page.complexity.medium`: 페이지에 렌더링 성능에 영향을 줄 수 있는 노드가 적당히 포함되어 있습니다.
* `page.complexity.high`: 페이지에 렌더링 성능에 영향을 줄 수 있는 노드가 매우 많이 포함되어 있습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 페이지 내에 있는 많은 양의 노드가 렌더링 성능에 영향을 줄 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 콘텐츠 구조를 검토하여 궁극적으로 페이지 렌더링 성능을 향상시키는 데 도움이 되도록 페이지 복잡성을 줄이는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 페이지 내에 있는 총 노드 수를 줄이려면 다음 단계를 따르십시오.
   * 불필요한 컨테이너가 있는지 확인합니다.
   * 더 적은 수의 컨테이너로 동일한 레이아웃을 구현할 수 있는지 테스트합니다.
   * 페이지 콘텐츠를 간소화합니다.
   * 노드 구조의 깊이를 줄입니다.
   * 포함된 경험 조각을 리팩터링하여 간소화합니다.
* 자세한 설명이 필요하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
