---
title: ECU
description: 패턴 감지기 코드 도움말 페이지
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: cbd43bca20831c19eb30703cc1ec528c75f2a2ef
workflow-type: ht
source-wordcount: '264'
ht-degree: 100%

---

# ECU {#ecu}

더 이상 사용되지 않는 기능: 불필요한 콘텐츠 사용 - CAV(콘텐츠 영역 위반)로 대체됨

## 배경 {#background}

`ECU`는 서로 다른 콘텐츠 영역이 콘텐츠 분류 규칙을 위반하는 방식으로 사용되는 패턴을 식별합니다.

Sling 요청 처리는 리소스의 콘텐츠(특히 `sling:resourceType` 속성)를 사용하여 콘텐츠 렌더링에 사용할 스크립트를 결정하는 방법을 정의합니다. 자세한 내용은 [스크립트 찾기](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script)를 참조하십시오. 또한 Sling은 “오버레이” 및 “오버라이드”를 통해 리소스에 액세스하고 리소스를 병합할 수 있는 기술을 제공합니다. 이러한 기술은 [Sling 리소스 병합](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) 및 [오버레이](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html)의 일부로 기술되어 있습니다.

고객이 `/libs`의 영역을 보다 안전하고 쉽게 이해할 수 있도록 `/libs`의 콘텐츠를 “mixin” 속성인 Public, Abstract, Final 및 Internal로 분류했습니다. 각각의 분류는 콘텐츠가 사용되거나, 상속되거나, 오버레이되는 방법에 대한 규칙을 나타냅니다. 자세한 설명은 [지속 가능한 업그레이드](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html)를 참조하십시오.

## 가능한 영향 및 위험 {#implications-and-risks}

* AEM 업그레이드 이후 페이지 렌더링 문제 및 기타 원하지 않은 비헤이비어가 발생할 수 있습니다.
* 보안 업데이트는 효과적이지 않습니다.

## 가능한 해결 방법 {#solutions}

* 콘텐츠 오버레이 사용을 필요한 경우로 최소화하십시오.
* 특히 제한된 콘텐츠(최종 및 내부 분류)를 오버레이하지 마십시오.
* AEM 업그레이드, ServicePack 또는 CumulativeFixPack 설치 이후 `/libs`에서 발생하는 변경 내용을 조정하는 것이 좋습니다.
* 자세한 설명이 필요하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
