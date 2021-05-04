---
title: DM
description: 패턴 탐지기 코드 도움말 페이지
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---

# DM {#dm}

다이내믹 미디어

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="다이내믹 미디어"
>abstract="DM 코드는 현재 구현에서 AEM Assets Dynamic Media의 사용을 식별합니다. Dynamic Media 모드는 실행 모드에서 감지됩니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="AEM 개발 - 지침 및 우수 사례"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="AEM as a Cloud Service 개발 지침"

`DM` AEM Assets Dynamic Media 사용을 식별합니다. Dynamic Media 모드는 실행 모드에서 감지됩니다.

하위 유형은 다음 코드와 함께 사용됩니다.

* `dynamic.media.runmode`:이 하위 유형의 연관된 값(제공된 경우)은 다음과 같습니다.
   * `dynamicmedia`:Dynamic Media - 하이브리드 모드
   * `dynamicmedia_scene7`:Dynamic Media - 장면 7 모드

## 가능한 의미 및 위험 {#implications-and-risks}

* `dynamic.media.runmode`
   * Dynamic Media과 관련된 업그레이드 문제가 있을 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="구현 지침"
>abstract="Cloud Service으로 AEM은 dynamicmedia_scene7 실행 모드만 지원합니다. 현재 설정을 검토하고 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Dynamic Media 설정"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"


* `dynamic.media.runmode`
   * 자세한 내용은 [Dynamic Media 설정](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html)에서 확인하십시오.

* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
