---
title: OU
description: 패턴 탐지기 코드 도움말 페이지
source-git-commit: fdc3e8bdef27de971743a9ecb04d3912cf8e60ad
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# OU {#ou}

오래된 사용

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="오래된 사용"
>abstract="Sling 또는 AEM 구성 요소나 API OSGi 내보내기 등의 일부 JCR 노드가 호환되지 않는 방식으로 변경되거나 제거되는 상황을 OU는 식별합니다. 고객은 업그레이드 전에 이러한 변경 사항을 알지 못할 수 있습니다. 호환되지 않는 버전으로 업그레이드하거나 전혀 사용할 수 없습니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주요 변경 사항 - AEM as a Cloud Service"

`OU` sling 또는 AEM 구성 요소나 API OSGi 내보내기 등의 일부 JCR 노드가 호환되지 않는 방식으로 변경 또는 제거되는 상황을 식별합니다. 고객은 업그레이드 전에 이러한 변경 사항을 알지 못할 수 있습니다. 호환되지 않는 버전으로 업그레이드하거나 전혀 사용할 수 없습니다.

이전 버전이 기본적으로 설치되지 않으므로 고객 애플리케이션이 제대로 작동하지 않을 수 있습니다.

## 가능한 의미와 위험 {#implications-and-risks}

* 더 이상 사용되지 않는 구성 요소 또는 API를 사용하는 모든 구성 요소에 종속되는 기능은 끊을 수 있으며 업그레이드 후 올바르게 확인되지 않을 수 있습니다.
* 고객 애플리케이션 또는 일부 AEM 기능의 일부 기능이 제대로 작동하지 않거나 업그레이드 후 활성 상태가 아닐 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 최신 버전의 AEM 구성 요소 또는 API를 사용하도록 고객 코드를 검토하고 조정하는 것입니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="Adobe Experience Manager SDK API"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 단기: 호환성 패키지를 설치하는 것이 도움이 될 수 있습니다.
* 장기: 최신 버전의 AEM 구성 요소 또는 API를 사용하도록 고객 코드를 조정하십시오.
* 연락하여 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) 명확히 하거나 문제를 해결하기 위해.
