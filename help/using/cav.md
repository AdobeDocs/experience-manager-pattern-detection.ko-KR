---
title: CAV
description: 패턴 감지기 코드 도움말 페이지
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 45%

---

# CAV {#cav}

콘텐츠 영역 위반

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="콘텐츠 영역 위반"
>abstract="CAV 코드는 서로 다른 콘텐츠 영역이 콘텐츠 분류 규칙을 위반하는 방식으로 사용되는 패턴을 식별합니다. 이 위반은 AEM으로 as a Cloud Service으로 이동한 후 변경해야 할 수 있는 오버레이 및 제한된 콘텐츠에 대한 개요를 제공합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling 리소스 병합"

CAV는 서로 다른 콘텐츠 영역이 콘텐츠 분류 규칙을 위반하는 방식으로 사용되는 패턴을 식별합니다.

Sling 요청 처리는 리소스의 콘텐츠 및 해당 콘텐츠를 정의하는 방법 `sling:resourceType` 특히, 속성은 콘텐츠 렌더링에 사용되는 스크립트를 결정하는 데 사용됩니다. 자세한 내용은 [스크립트 찾기](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script)를 참조하십시오. 또한 Sling은 “오버레이” 및 “오버라이드”를 통해 리소스에 액세스하고 리소스를 병합할 수 있는 기술을 제공합니다. 이러한 기술은 [Sling 리소스 병합](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) 및 [오버레이](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays)의 일부로 기술되어 있습니다.

고객이 의 영역을 보다 안전하고 쉽게 이해할 수 있도록 지원 `/libs` 콘텐츠를 사용하고 오버레이하는 것이 안전합니다. `/libs` 은 &quot;mixin&quot; 속성인 Public, Abstract, Final 및 Internal로 분류되었습니다. 각각의 분류는 콘텐츠가 사용되거나, 상속되거나, 오버레이되는 방법에 대한 규칙을 나타냅니다. 자세한 설명은 [지속 가능한 업그레이드](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades)를 참조하십시오.

## 가능한 영향 및 위험 {#implications-and-risks}

* AEM 업그레이드 이후 페이지 렌더링 문제 및 기타 원하지 않은 비헤이비어가 발생할 수 있습니다.
* 보안 업데이트는 효과적이지 않습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="구현 지침"
>abstract="CAS를 통해 식별된, 서로 다른 콘텐츠 영역 위반 이 존재하는 패턴을 검토해야 합니다. 최종 및 내부 콘텐츠 분류 영역을 피해야 합니다. 도움 또는 설명이 필요한 경우 Adobe 지원 센터에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="지속 가능한 업그레이드"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 콘텐츠 오버레이 사용을 필요한 경우로 최소화하십시오.
* 특히 제한된 콘텐츠(최종 및 내부 분류)를 오버레이하지 마십시오.
* 다음에서 발생하는 변경 사항을 조정하는 것이 좋습니다. `/libs` AEM 업그레이드 후 서비스 팩 또는 누적 수정 팩 설치
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
