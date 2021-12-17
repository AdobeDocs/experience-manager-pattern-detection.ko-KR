---
title: NCC
description: 패턴 탐지기 코드 도움말 페이지
source-git-commit: fdc3e8bdef27de971743a9ecb04d3912cf8e60ad
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 4%

---

# NCC {#ncc}

호환되지 않는 변경 사항

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="호환되지 않는 변경 사항"
>abstract="NCC는 일부 JCR 노드 또는 번들이 호환되지 않는 방식으로 변경되는 상황을 식별합니다. 고객은 업그레이드 전에 이러한 변경 사항을 알지 못할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주요 변경 사항 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR" text="릴리스 노트 - AEM as a Cloud Service"

`NCC` 는 일부 JCR 노드 또는 번들이 호환되지 않는 방식으로 변경되는 상황을 식별합니다. 고객은 업그레이드 전에 이러한 변경 사항을 알지 못할 수 있습니다.

## 가능한 의미와 위험 {#implications-and-risks}

* 호환되지 않는 변경 사항을 사용하는 모든 구성 요소에 종속되는 기능은 손상되어 올바르게 해결되지 않을 수 있습니다.
* 업그레이드 후 고객 애플리케이션 또는 일부 AEM 기능이 제대로 작동하지 않을 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="구현 지침"
>abstract="우수 사례는 사용자 지정 코드를 검토하고 호환되는 Sling 구성 요소만 오버레이되거나 참조되도록 하는 것입니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="오버레이"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 호환 가능한 Sling 구성 요소만 오버레이 또는 참조합니다.
* 자원 채택 `/libs` 또는 AEM 업그레이드 후 번들을 포함할 수 있습니다.
* 연락하여 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) 명확히 하거나 문제를 해결하기 위해.
