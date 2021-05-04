---
title: LOCP
description: 패턴 탐지기 코드 도움말 페이지
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# LOCP {#locp}

/libs 사용자 정의 패키지 덮어쓰기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs 사용자 정의 패키지 덮어쓰기"
>abstract="LOCP는 /libs에 컨텐츠를 전달하는 사용자 지정 패키지 검색을 식별합니다(ACL의 경우 제외)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="지속적인 업그레이드"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Sling 자원 통합"

`LOCP` 컨텐츠를 전달하는 사용자 지정 패키지 검색을  `/libs`식별합니다(ACL의 경우 제외).

## 가능한 의미 및 위험 {#implications-and-risks}

* 모든 CFP, SP 또는 주요 AEM 업그레이드에 대해 고객 코드를 삭제하거나 교체할 수 있습니다.
* 경우에 따라 새 콘텐트가 제대로 설치되지 않을 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="구현 지침"
>abstract="고객은 맞춤형 코드와 패키지를 검토하여 컨텐츠가 /libs에 제공되는지 확인하고 /apps 아래의 컨텐츠를 오버레이하여 AEM과 Cloud Service으로 호환되도록 리팩터링해야 합니다. 도움말 및 분류에 대한 Adobe 지원"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="오버레이"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 고객 패키지는 `/libs` 대신 `/apps`에 콘텐츠를 배포해야 합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
