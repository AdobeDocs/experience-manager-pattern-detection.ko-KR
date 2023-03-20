---
title: NCC
description: 패턴 감지기 코드 도움말 페이지
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 8b8d902dc5b5a8534475d256c199dc235bb35464
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 100%

---

# NCC {#ncc}

호환되지 않는 변경 내용

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="호환되지 않는 변경 내용"
>abstract="NCC는 일부 JCR 노드 또는 번들이 호환되지 않는 방식으로 변경되는 상황을 식별합니다. 고객은 업그레이드 전 이러한 변경 내용에 대해 알지 못할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="릴리스 정보 - AEM as a Cloud Service"

`NCC`는 일부 JCR 노드 또는 번들이 호환되지 않는 방식으로 변경되는 상황을 식별합니다. 고객은 업그레이드 전 이러한 변경 내용에 대해 알지 못할 수 있습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 호환되지 않는 변경 내용을 사용하는 구성 요소에 의존하는 기능이 중단되어 올바르게 해결되지 않을 수 있습니다.
* 고객 애플리케이션의 일부 기능 또는 일부 AEM 기능이 업그레이드 이후 제대로 작동하지 않을 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 사용자 지정 코드를 검토한 다음 호환되는 Sling 구성 요소만 오버레이 또는 참조하는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="오버레이"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 호환되는 Sling 구성 요소만 오버레이하거나 참조하십시오.
* AEM 업그레이드 이후 `/libs` 또는 번들 내의 리소스를 사용하는 것이 좋습니다.
* 자세한 설명이 필요하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
