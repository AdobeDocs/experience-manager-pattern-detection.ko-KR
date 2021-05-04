---
title: IOI
description: 패턴 탐지기 코드 도움말 페이지
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# IOI {#ioi}

내부 Oak 가져오기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="내부 Oak 가져오기"
>abstract="IOI 코드는 OSGi를 통해 내부 Oak 패키지를 가져와 고객이 내부 Oak 패키지를 사용하는 경우를 식별합니다. 일반적으로 특정 버전 없이 내보내지며 다른 Oak 번들 또는 저수준 AEM 서비스에서만 사용하도록 만들어졌습니다."

`IOI` OSGi를 통해 고객이 내부 Oak 패키지를 사용하도록 식별합니다. 일반적으로 특정 버전 없이 내보내지며 다른 Oak 번들 또는 저수준 AEM 서비스에서만 사용하도록 만들어졌습니다.

이러한 항목 중 일부는 `com.adobe.granite.repository`에서 사용되며, 이 저장소를 사용하여 시작하는 동안 AEM에 대한 저장소를 설정합니다. 또 다른 예로 `com.adobe.granite.maintenance.oak` Adobe 번들을 들 수 있습니다. 번들은 래핑되며 Oak 유지 관리 작업을 제공합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 향후 AEM 버전 내부 내보내기는 Oak에 따라 끊어진 종속성 및 비활성 번들로 인해 제거될 수 있습니다.
* 내부 내보내기의 API가 변경될 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="구현 지침"
>abstract="고객은 자신의 사용자 지정 코드를 검토하여 이러한 API의 사용을 식별해야 하며 AEM과 Cloud Service의 호환성을 고려해야 합니다. 도움말 및 분류에 대한 Adobe 지원"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 낮은 수준의 액세스 대신 Sling 리소스 API(또는 JCR API)를 사용하십시오.
* 공용 API 또는 SPI에 속하지 않는 내부 패키지에 의존하지 마십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
