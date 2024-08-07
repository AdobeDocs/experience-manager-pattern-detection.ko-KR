---
title: NBCC
description: 패턴 감지기 코드 도움말 페이지.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# NBCC {#nbcc}

더 이상 사용되지 않는 기능: 역으로 호환되지 않는 변경 내용 - NCC(호환되지 않는 변경 내용)으로 대체됨

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="역으로 호환되지 않는 변경 내용"
>abstract="NBCC는 일부 JCR 노드 또는 번들이 호환되지 않는 방식으로 변경되는 상황을 식별합니다. 고객은 업그레이드하기 전에 이러한 변경 내용에 대해 알지 못할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="릴리스 정보 - AEM as a Cloud Service"

`NBCC`는 일부 JCR 노드 또는 번들이 호환되지 않는 방식으로 변경되는 상황을 식별합니다. 고객은 업그레이드하기 전에 이러한 변경 내용에 대해 알지 못할 수 있습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 역으로 호환되지 않는 변경 내용을 사용하는 구성 요소에 의존하는 기능이 중단되어 올바르게 해결되지 않을 수 있습니다.
* 고객 애플리케이션의 일부 기능 또는 일부 AEM 기능이 업그레이드 이후 제대로 작동하지 않을 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 사용자 정의 코드를 검토한 다음, 역으로 호환되는 Sling 구성 요소만 오버레이 또는 참조하는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="오버레이"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 역으로 호환되는 Sling 구성 요소만 오버레이하거나 참조하십시오.
* AEM 업그레이드 이후 `/libs` 또는 번들 내의 리소스를 사용하는 것이 좋습니다.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
