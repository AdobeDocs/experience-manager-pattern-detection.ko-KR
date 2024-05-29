---
title: OU
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: ht
source-wordcount: '270'
ht-degree: 100%

---

# OU {#ou}

오래된 사용

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="오래된 사용"
>abstract="OU는 Sling, AEM 구성 요소 또는 API OSGi 내보내기와 같은 일부 JCR 노드가 호환되지 않는 방식으로 변경되거나 제거되는 상황을 식별합니다. 고객은 업그레이드하기 전에 이러한 변경 내용에 대해 알지 못할 수 있습니다. 이들 노드는 호환되지 않는 버전으로 업그레이드되거나 아예 사용하지 못하게 될 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="주요 변경 내용 - AEM as a Cloud Service"

`OU`는 Sling, AEM 구성 요소 또는 API OSGi 내보내기와 같은 일부 JCR 노드가 호환되지 않는 방식으로 변경되거나 제거되는 상황을 식별합니다. 고객은 업그레이드하기 전에 이러한 변경 내용에 대해 알지 못할 수 있습니다. 이들 노드는 호환되지 않는 버전으로 업그레이드되거나 아예 사용하지 못하게 될 수 있습니다.

이전 버전이 기본적으로 설치되어 있지 않으므로, 고객 애플리케이션이 제대로 작동하지 않을 수 있습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 더 이상 사용되지 않는 구성 요소 또는 API를 사용하는 구성 요소에 의존하는 기능이 업그레이드 이후 중단되어 올바르게 해결되지 않을 수 있습니다.
* 고객 애플리케이션의 일부 기능 또는 일부 AEM 기능이 업그레이드 이후 제대로 작동하지 않거나 활성화되지 않을 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 고객 코드를 검토 및 조정하여 최신 버전의 AEM 구성 요소 또는 API를 사용하는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="Adobe Experience Manager SDK API"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 단기적 지원: 호환성 패키지를 설치하십시오.
* 장기적 지원: 고객 코드를 조정하여 최신 버전의 AEM 구성 요소 또는 API를 사용하십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
