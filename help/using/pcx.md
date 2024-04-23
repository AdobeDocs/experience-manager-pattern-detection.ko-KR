---
title: PCX
description: 패턴 감지기 코드 도움말 페이지
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 53%

---

# PCX {#pcx}

페이지 복잡성

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="페이지 복잡성"
>abstract="PCX는 구조에 대량의 노드가 포함된 페이지를 식별합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - 릴리스 정보"

PCX는 구조에 많은 노드가 포함된 페이지를 식별합니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `page.complexity.medium`: 페이지에 렌더링 성능에 영향을 줄 수 있는 노드가 적당히 포함되어 있습니다.
* `page.complexity.high`: 페이지에 렌더링 성능에 영향을 줄 수 있는 노드가 많이 포함되어 있습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 페이지 내의 많은 노드가 렌더링 성능에 영향을 줄 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 컨텐츠 구조를 검토하여 페이지 복잡성을 줄이는 것입니다. 이를 통해 페이지 렌더링 성능을 개선하는 데 도움이 됩니다. 도움 또는 설명이 필요한 경우 Adobe 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 다음 작업을 수행하여 페이지 내 총 노드 수를 줄입니다.
   * 불필요한 컨테이너가 있는지 확인합니다.
   * 더 적은 수의 컨테이너로 동일한 레이아웃을 구현할 수 있는지 테스트합니다.
   * 페이지 콘텐츠를 간소화합니다.
   * 노드 구조의 깊이를 줄입니다.
   * 포함된 경험 조각을 리팩터링하여 간소화합니다.
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
