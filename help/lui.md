---
title: LUI
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 5%

---

# LUI {#lui}

기존 사용자 인터페이스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="기존 사용자 인터페이스"
>abstract="LUI는 나중에 AEM 및 AEM as a Cloud Service에서 권장되지 않거나 지원되지 않는 사용 중단되는 사용자 인터페이스 요소의 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주요 변경 사항 - AEM as a Cloud Service"

`LUI` 는 이후 버전의 AEM 및 AEM as a Cloud Service에서 권장되지 않거나 지원되지 않는 사용 중단되는 사용자 인터페이스 요소의 사용을 식별합니다.

하위 유형은 업그레이드해야 하거나 업그레이드해야 하는 다양한 유형의 사용자 인터페이스 요소를 식별하는 데 사용됩니다.

* `legacy.dialog.classic`:ExtJS를 기반으로 하는 클래식 UI 대화 상자는 Coral로 변경해야 합니다.
   * 대화 상자 이름이 &quot;dialog&quot; 또는 &quot;design_dialog&quot;이고
`jcr:primaryType` 속성 값 또는 `xtype` 속성 값은 &quot;cq:Dialog&quot;입니다.
* `legacy.dialog.coral2`:Coral 2 대화 상자는 Coral 3을 사용하도록 업데이트해야 합니다.
   * 대화 상자 및 해당 하위 컨텐츠 노드 이름이 &quot;cq:dialog/content&quot;일 때 감지됩니다.
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot; 또는 &quot;cq:design_dialog.coral2/content&quot;
및 `sling:resourceType` 속성 값이 다음을 포함하지 않습니다
&quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`:에서 상속되는  `foundation/components`구성 요소는 핵심 구성 요소를 사용하도록 업데이트해야 합니다.
   * 이는 `jcr:primaryType` 속성 값이 &quot;cq:Component&quot;이고
      `sling:resourceSuperType` 속성 값에 &quot;foundation/components&quot; 또는 다음 중 하나가 포함됩니다
      `sling:resourceSuperType` 상위 유형 구성 요소 체인의 속성 값에 &quot;foundation/components&quot;가 포함됩니다.
* `legacy.static.template`:정적 템플릿 을 편집 가능한 템플릿으로 업그레이드해야 합니다.
   * 이는 `jcr:primaryType` 속성 값이 &quot;cq:Template&quot;일 때 감지됩니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="구현 지침"
>abstract="클래식 UI는 AEM에서 더 이상 Cloud Service으로 사용할 수 없으며 작성을 위한 표준 인터페이스는 터치 지원 UI입니다. Best Practice는 지원되지 않는 모든 인터페이스를 이동하는 것이며 연결된 고객은 AEM as a Cloud Service과 호환되는 최신 기능/기능으로 리팩터링해야 합니다. 고객은 기존 AEM 현대화 Suite를 활용하여 AEM Sites 구현을 현대화하는 데 필요한 노력을 줄일 수 있습니다."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM 현대화 도구"

* 클래식 UI는 AEM에서 더 이상 Cloud Service으로 사용할 수 없습니다. 작성을 위한 표준 인터페이스는 터치 지원 UI입니다.
* 기존 사용자 지정 구성 요소에 의존하면 시간이 지남에 따라 유지 관리 비용이 늘어날 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="도구 및 리소스"
>abstract="AEM 현대화 제품군의 도움으로 고객은 클래식(ExtJS) 대화 상자를 Coral 대화 상자로 변환할 수 있습니다. 고객이 지원되지 않거나 레거시 기능에서 강력하고 최신 AEM 오퍼링으로 이동할 수 있도록 지원하기 위한 것입니다. 이러한 도구는 구성, 구성 인식 및 확장 가능합니다. 또한 표준 핵심 구성 요소 집합으로 사용자 정의 구성 요소를 교체하여 개발 시간을 단축하고 애플리케이션의 유지 관리 비용을 절감할 수 있습니다."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="구성 요소 변환기"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="코어 구성 요소"

* [AEM 현대화 도구 세트](https://opensource.adobe.com/aem-modernize-tools/)를 활용하여 AEM Sites 구현을 현대화하는 데 필요한 노력을 줄이십시오. 이러한 도구에는 전환 기능이 포함됩니다.
   * Coral 대화 상자에 대한 클래식(ExtJS) 대화 상자
   * 기초 구성 요소를 코어 구성 요소
   * 편집 가능한 템플릿 및 응답형 그리드에 정적 템플릿 및 열 컨트롤
   * 편집 가능한 템플릿 정책에 대한 디자인 및 디자인 대화 상자
* 프로젝트의 사용자 지정 구성 요소 라이브러리와 전환(가능한 경우)을 표준화된 [핵심 구성 요소](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=ko-KR) 집합으로 검토하여 개발 시간을 단축하고 애플리케이션의 유지 관리 비용을 절감합니다.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
