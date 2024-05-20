---
title: DM
description: 패턴 감지기 코드가 AEM Assets - Dynamic Media의 사용을 식별하는 방법에 대해 알아봅니다.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 78%

---

# DM {#dm}

Dynamic Media

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="DM 코드는 현재 구현에서의 AEM Assets Dynamic Media 사용을 식별합니다. 실행 모드는 Dynamic Media 모드를 감지합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="AEM 개발 - 지침 및 우수 사례"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="AEM as a Cloud Service 개발 지침"

`DM`(Dynamic Media)은 AEM Assets Dynamic Media 사용을 식별합니다. 실행 모드는 Dynamic Media 모드를 감지합니다.

하위 유형이 이 코드와 함께 사용됩니다.

* `dynamic.media.runmode`: 이 하위 유형의 관련 값은 다음 중 하나입니다.
   * `dynamicmedia`: Dynamic Media - 하이브리드 모드
   * `dynamicmedia_scene7`: Dynamic Media - Scene7 모드

## 가능한 영향 및 위험 {#implications-and-risks}

* `dynamic.media.runmode`
   * Dynamic Media 관련 업그레이드 문제가 발생할 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="구현 지침"
>abstract="AEM as a Cloud Service는 dynamicmedia_scene7 실행 모드만 지원합니다. 현재 설정을 검토하고 Adobe 지원 팀에 연락하여 도움 및 설명을 요청하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Dynamic Media 설정"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"


* `dynamic.media.runmode`
   * 자세한 내용은 [Dynamic Media 설정](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media)을 참조하십시오.

* 자세한 설명이나 문제 해결이 필요한 경우 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
