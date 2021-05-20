---
title: CAV
description: 패턴 탐지기 코드 도움말 페이지
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CAV {#cav}

콘텐츠 영역 위반

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="콘텐츠 영역 위반"
>abstract="CAV 코드는 컨텐츠 분류 규칙을 위반하는 방식으로 서로 다른 컨텐츠 영역이 사용되는 패턴을 식별합니다. 이 위반은 Cloud Service으로 AEM으로 이동한 후 변경해야 할 수 있는 오버레이, 제한된 컨텐츠에 대한 개요를 제공합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Sling Resource Merger"

`CAV` 컨텐츠 분류 규칙을 위반하는 방식으로 서로 다른 컨텐츠 영역이 사용되는 패턴을 식별합니다.

Sling 요청 처리에서는 리소스의 컨텐츠, 특히 `sling:resourceType` 속성을 사용하여 컨텐츠를 렌더링하는 데 사용할 스크립트를 결정하는 방법을 정의합니다. 자세한 내용은 [스크립트](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) 찾기 를 참조하십시오. Sling은 &quot;오버레이&quot; 및 &quot;무시&quot;를 통해 리소스에 액세스하고 병합하는 기술을 제공합니다. 이러한 내용은 [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) 및 [Overlays](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html)의 일부로 설명되어 있습니다.

고객이 안전하고 쉽게 `/libs`의 어떤 영역을 안전하게 사용하고 `/libs`에 있는 컨텐츠가 &quot;mixin&quot; 속성으로 분류되었는지 알 수 있도록 하기 위해:Public, Abstract, Final 및 Internal. 각 분류는 컨텐츠가 사용자, 상속 또는 오버레이될 수 있는 방법에 대한 규칙을 의미합니다. 자세한 내용은 [지속 가능 업그레이드](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) 를 참조하십시오.

## 가능한 의미 및 위험 {#implications-and-risks}

* AEM 업그레이드로 인해 페이지 렌더링 문제 및 기타 원치 않는 동작이 발생할 수 있습니다.
* 보안 업데이트가 적용되지 않습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="구현 지침"
>abstract="서로 다른 컨텐츠 영역 위반이 존재하는 CAS로 식별된 패턴을 검토해야 합니다. 최종 및 내부 컨텐츠 분류 영역은 피해야 합니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="지속 가능한 업그레이드"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 필요한 경우에 컨텐츠 오버레이의 사용을 최소화하십시오.
* 특히 제한된 컨텐츠(최종 및 내부 분류)를 오버레이하지 마십시오.
* AEM 업그레이드, 서비스 팩 또는 누적 수정 팩 설치 후 `/libs`에서 오는 변경 사항을 수정하는 것이 좋습니다.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
