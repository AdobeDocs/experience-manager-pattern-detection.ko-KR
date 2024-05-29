---
title: LOCP
description: 패턴 감지기 코드 도움말 페이지.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: ht
source-wordcount: '168'
ht-degree: 100%

---

# LOCP {#locp}

/libs 맞춤형 패키지 덮어쓰기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs 맞춤형 패키지 덮어쓰기"
>abstract="LOCP는 콘텐츠에 앤티 패턴인 `/libs`를 제공하는 맞춤형 패키지 감지를 식별합니다(ACL가 있는 경우 제외)."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="지속 가능한 업그레이드"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling 리소스 병합"

`LOCP`는 콘텐츠에 앤티 패턴인 `/libs`를 제공하는 맞춤형 패키지 감지를 식별합니다(ACL의 경우 제외).

## 가능한 영향 및 위험 {#implications-and-risks}

* 사용자 정의 코드가 CFP, SP 또는 주요 AEM 업그레이드를 위해 삭제되거나 대체될 수 있습니다.
* 경우에 따라 새 콘텐츠가 제대로 설치되지 않을 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="구현 지침"
>abstract="고객은 사용자 정의 코드 및 패키지를 검토하여 콘텐츠가 `/libs`로 전달되는지 확인해야 합니다. 필요한 경우, /apps 아래의 콘텐츠 오버레이를 사용하고, AEM as a Cloud Service와 호환되도록 리팩터링하십시오. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="오버레이"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 고객 패키지는 `/libs`가 아닌 `/apps`에 콘텐츠를 배포해야 합니다.
* 자세한 설명이나 문제 해결이 필요한 경우 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
