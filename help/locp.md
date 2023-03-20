---
title: LOCP
description: 패턴 감지기 코드 도움말 페이지
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 100%

---

# LOCP {#locp}

/libs 맞춤형 패키지 덮어쓰기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs 맞춤형 패키지 덮어쓰기"
>abstract="LOCP는 콘텐츠에 앤티 패턴인 /libs를 제공하는 맞춤형 패키지 감지를 식별합니다(ACL의 경우 제외)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="지속 가능한 업그레이드"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Sling 리소스 병합"

`LOCP`는 콘텐츠에 앤티 패턴인 `/libs`를 제공하는 맞춤형 패키지 감지를 식별합니다(ACL의 경우 제외).

## 가능한 영향 및 위험 {#implications-and-risks}

* 사용자 지정 코드가 CFP, SP 또는 주요 AEM 업그레이드를 위해 삭제되거나 대체될 수 있습니다.
* 경우에 따라 새 콘텐츠가 올바르게 설치되지 않을 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="구현 지침"
>abstract="고객은 사용자 지정 코드 및 패키지를 검토하여 콘텐츠가 /libs에 전달되었는지 확인하고 /apps 하의 콘텐츠 위에 오버레이되도록 리팩터링하여 AEM as a Cloud Service와 호환되도록 해야 합니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="오버레이"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 고객 패키지는 `/libs`가 아닌 `/apps`에 콘텐츠를 배포해야 합니다.
* 자세한 설명이 필요하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
