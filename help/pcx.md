---
title: PCX
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# PCX {#pcx}

페이지 복잡도

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="페이지 복잡도"
>abstract="PCX는 해당 구조에 많은 수의 노드가 포함된 페이지를 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주목할 만한 변경 사항 - Cloud Service으로 AEM"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR" text="AEM을 Cloud Service - 릴리스 노트"

`PCX` 해당 구조에 많은 수의 노드가 포함된 페이지를 식별합니다.

하위 유형은 서로 다른 유형의 정보를 식별하는 데 사용됩니다.

* `page.complexity.medium`:페이지에 렌더링 성능에 영향을 줄 수 있는 노드가 상당히 많이 포함되어 있습니다.
* `page.complexity.high`:페이지에 렌더링 성능에 영향을 줄 매우 많은 수의 노드가 포함되어 있습니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 페이지 내의 노드 수가 많으면 렌더링 성능에 영향을 줄 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 컨텐츠 구조를 검토하여 페이지의 복잡성을 줄이고 페이지 렌더링 성능을 향상시키는 것입니다. 도움말 및 분류에 대한 Adobe 지원"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 다음을 포함하여 페이지 내의 총 노드 수를 줄이는 단계를 수행합니다.
   * 불필요한 컨테이너가 없는지 확인합니다.
   * 컨테이너 수를 줄여 동일한 레이아웃을 만들 수 있는지 여부를 테스트합니다.
   * 페이지 컨텐츠를 간소화할 수 있습니다.
   * 노드 구조의 깊이를 줄입니다.
   * 포함된 경험 조각을 간단하게 리팩터링할 수 있습니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
