---
title: CCOM
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 84%

---

# CCOM {#ccom}

사용자 지정 구성 요소

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="사용자 지정 구성 요소"
>abstract="CCOM은 AEM에 설치된 사용자 지정 구성 요소를 식별합니다. 이 정보는 모범 사례 평가 목적으로 제공됩니다."

`CCOM` AEM에 설치된 사용자 지정 구성 요소를 식별합니다. 이 정보는 모범 사례 평가 목적으로 제공됩니다.

구성 요소의 범주를 식별하기 위해 하위 유형이 이 코드와 함께 사용됩니다.

* `custom.core`: 구성 요소의 슈퍼타입 체인 내에 있는 슈퍼타입에는 “core/wcm/components/”가 포함되며, 이는 해당 슈퍼타입이 핵심 구성 요소로부터 상속받음을 나타냅니다.
* `custom.foundation`: 구성 요소의 슈퍼타입 체인 내에 있는 슈퍼타입에는 “core/wcm/components/”가 포함되며, 이는 해당 슈퍼타입이 핵심 구성 요소로부터 상속받음을 나타냅니다.
* `custom.overlay.foundation`: 구성 요소 패스에는 “wcm/foundation/components/” 또는 “foundation/components/”가 포함되며, 이는 해당 구성 요소 패스가 기초 구성 요소에 오버레이됨을 나타냅니다.
* `custom`: 사용자 지정 구성 요소는 핵심 또는 기초 구성 요소를 상속받거나 핵심 또는 기초 구성 요소에 오버레이되지 않습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 가장 좋은 방법은 사용자 지정 구성 요소의 수를 최소화하고, 핵심 구성 요소를 사용하고, 핵심 구성 요소와 스타일 시스템을 함께 사용하여 기술적인 문제를 줄이는 것입니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 사용자 정의 구성 요소의 수를 최소화하고, 핵심 구성 요소를 사용하고, 핵심 구성 요소와 스타일 시스템을 함께 사용하여 기술적인 부담을 줄이는 것입니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-core-components/using/introduction" text="핵심 구성 요소"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="스타일 시스템"

* [핵심 구성 요소 소개](https://experienceleague.adobe.com/ko/docs/experience-manager-core-components/using/introduction)에서 핵심 구성 요소에 대해 자세히 알아보십시오.
* [스타일 시스템 사용](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring)에서 스타일 시스템에 대해 자세히 알아보십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
