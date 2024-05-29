---
title: IOI
description: 패턴 감지기 코드 도움말 페이지.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: ht
source-wordcount: '212'
ht-degree: 100%

---

# IOI {#ioi}

내부 Oak 가져오기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="내부 Oak 가져오기"
>abstract="IOI 코드는 내부 Oak 패키지의 고객 사용을 식별하며 OSGi를 통해 해당 패키지를 가져옵니다. 특정 버전을 사용하지 않고 내보내집니다. Oak 번들 또는 낮은 수준의 AEM 서비스만 사용합니다."

`IOI`는 내부 Oak 패키지의 고객 사용을 식별하며 OSGi를 통해 해당 패키지를 가져옵니다. 특정 버전을 사용하지 않고 내보내집니다. Oak 번들 또는 낮은 수준의 AEM 서비스만 사용합니다.
이러한 영역 중 일부는 시작 시 AEM에 저장소를 설정하는 `com.adobe.granite.repository`에서 사용됩니다. 또 다른 예는 Oak 유지 관리 작업을 래핑 및 제공하는 `com.adobe.granite.maintenance.oak` Adobe 번들입니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 향후 AEM 버전에서는 내부 내보내기 기능이 제거되어 전적으로 Oak에 따라 종속성이 끊어지고 번들이 비활성화될 수 있습니다.
* 내부 내보내기의 API는 변경될 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="구현 지침"
>abstract="고객은 사용자 정의 코드를 검토하여 이러한 API의 사용을 식별하고 이를 AEM as a Cloud Service와 호환되도록 리팩터링해야 합니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 낮은 수준의 액세스 대신 Sling 리소스 API(또는 JCR API)를 사용하십시오.
* 공개 API 또는 SPI의 일부가 아닌 내부 패키지에 의존하지 않도록 하십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
