---
title: CAV
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# CAV {#cav}

콘텐츠 영역 위반

## 배경 {#background}

`CAV` 컨텐트 분류 규칙을 위반하는 방법으로 서로 다른 컨텐트 영역이 사용되는 패턴을 식별합니다.

Sling 요청 처리는 리소스 내용(특히 `sling:resourceType` 속성)을 사용하여 컨텐츠를 렌더링하는 데 사용할 스크립트를 결정하는 방법을 정의합니다. 자세한 내용은 [스크립트](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) 찾기를 참조하십시오. 또한 Sling은 &quot;Overlays&quot; 및 &quot;Overrides&quot;를 통해 리소스에 액세스하고 병합하는 기법을 제공합니다. 이러한 사항은 [Sling 리소스 합병](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html)의 일부와 [Overlays](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html)에서 설명합니다.

고객이 `/libs`의 어떤 영역을 안전하고 쉽게 사용하고 `/libs`의 컨텐트를 &quot;mixin&quot; 속성으로 분류했는지 알 수 있도록 하기 위해.공개, 개요, 최종 및 내부. 각 분류는 컨텐츠가 사용자, 상속 또는 오버레이될 수 있는 방법에 대한 규칙을 의미합니다. 자세한 설명은 [지속 가능한 업그레이드](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html)를 참조하십시오.

## 가능한 의미 및 위험 {#implications-and-risks}

* AEM 업그레이드로 인해 페이지 렌더링 문제 및 기타 원치 않는 동작이 발생할 수 있습니다.
* 보안 업데이트가 유효하지 않습니다.

## 가능한 솔루션 {#solutions}

* 필요한 경우 내용 오버레이의 사용을 최소화할 수 있습니다.
* 특히, 제한된 컨텐츠(최종 및 내부 분류)를 오버레이하지 마십시오.
* AEM 업그레이드, ServicePack 또는 CumulativeFixPack 설치 후 `/libs`에서 오는 변경 사항을 적용하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
