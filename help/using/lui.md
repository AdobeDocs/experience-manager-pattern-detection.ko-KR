---
title: LUI
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 96%

---

# LUI {#lui}

기존 사용자 인터페이스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="기존 사용자 인터페이스"
>abstract="LUI는 최신 버전의 AEM 및 AEM as a Cloud Service에서 권장되거나 지원되지 않는, 더 이상 사용되지 않는 사용자 인터페이스 요소의 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="주요 변경 내용 - AEM as a Cloud Service"

`LUI`  는 최신 버전의 AEM 및 AEM as a Cloud Service에서 권장되거나 지원되지 않는, 더 이상 사용되지 않는 사용자 인터페이스 요소의 사용을 식별합니다.

업그레이드해야 하는 다양한 유형의 사용자 인터페이스 요소를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `legacy.dialog.classic`: ExtJS 기반의 클래식 UI 대화 상자를 식별하며, 코랄로 변경해야 합니다.
   * 이는 대화 상자 이름이 “dialog” 또는 “design_dialog”이며 `jcr:primaryType` 속성 값 또는 `xtype` 속성 값이 `cq:Dialog`인 경우 감지됩니다.
* `legacy.dialog.coral2`: `Coral 3`를 사용하려면 `Coral 2` 대화 상자를 업데이트해야 합니다.
   * 이는 대화 상자와 해당 하위 콘텐츠 노드 이름이 `cq:dialog/content`,
     `cq:design_dialog/content`, `cq:dialog.coral2/content` 또는 `cq:design_dialog.coral2/content`이며 `sling:resourceType` 속성 값에 “granite/ui/components/coral/foundation”이 포함되지 않은 경우 감지됩니다.
* `legacy.custom.component`: `foundation/components`로부터 상속받는 구성 요소를 식별하며, 핵심 구성 요소를 사용하도록 업데이트해야 합니다.
   * 이는 `jcr:primaryType` 속성 값이 “`cq:Component`”이며
     `sling:resourceSuperType` 속성 값에 “foundation/components”가 포함되어 있는 경우 감지됩니다. 또는
     슈퍼타입 구성 요소 체인의 `sling:resourceSuperType` 속성 값에 “foundation/components”가 포함되어 있는 경우 감지됩니다.
* `legacy.static.template`: 정적 템플릿을 식별하며, 편집 가능한 템플릿으로 업그레이드해야 합니다.
   * 이는 `jcr:primaryType` 속성 값이 “`cq:Template`”인 경우 감지됩니다.
* `content.fragment.template`: 콘텐츠 조각 템플릿이 조각 템플릿을 대체할 조각 모델을 생성해야 합니다.
   * 콘텐츠 조각 템플릿은 다음 위치에서 찾을 수 있습니다.
      * 기본 제공 콘텐츠 조각 템플릿은 `/libs/settings/dam/cfm/templates`에 저장됩니다.
      * 이는 `/apps/settings/dam/cfm/templates` 또는 `/conf/.../settings/dam/cfm/templates`(... = global 또는 &quot;tenant&quot;)에 오버레이할 수 있습니다.
* `translation.dictionary`: /apps 아래에 `I18n` 전이 표시됩니다.
   * /apps가 런타임에 변경되지 않으며 translator.html을 더 이상 AEM as a Cloud Service에서 사용할 수 없습니다.

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="구현 지침"
>abstract="클래식 UI는 더 이상 AEM as a Cloud Service에서 사용할 수 없으며, 제작을 위한 표준 인터페이스는 터치 기능이 지원되는 UI입니다. 가장 좋은 방법은 지원되지 않는 모든 인터페이스를 이동하고 연결된 맞춤화를 AEM as a Cloud Service와 호환되는 새로운 기능에 리팩터링하는 것입니다. 기존 AEM 현대화 제품군을 사용하여 AEM Sites 구현을 현대화하는 데 필요한 수고를 줄일 수 있습니다."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="AEM 현대화 도구"

* 클래식 UI는 AEM as a Cloud Service에서 더 이상 사용할 수 없습니다. 제작을 위한 표준 인터페이스는 터치 기능이 지원되는 UI입니다.
* 기존 사용자 지정 구성 요소에 의지하면 시간이 지남에 따라 유지 관리에 더 많은 비용이 필요하게 될 수 있습니다.
* 콘텐츠 조각 템플릿은 AEM 6.3에서 콘텐츠 조각 모델로 대체되었습니다. 레거시 템플릿을 기반으로 하는 콘텐츠 조각을 AEM as a Cloud Service로 마이그레이션하면 이들 조각은 기능적으로 유지되지만 레거시 템플릿을 기반으로 하는 조각은 생성할 수 없습니다. 또한 스키마로 콘텐츠 조각 모델을 필요로 하는 AEM GraphQL을 사용하여 이들 조각을 전달할 수 없습니다.
* /apps가 런타임에 변경되지 않으며 translator.html을 더 이상 AEM as a Cloud Service에서 사용할 수 없습니다. 따라서 CI/CD 파이프라인을 통해 Git에서 `I18n` 사전을 가져와야 합니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="도구 및 리소스"
>abstract="AEM 현대화 제품군을 통해 클래식(ExtJS) 대화 상자를 코랄 대화 상자로 변환할 수 있습니다. 이는 고객이 지원되지 않는 또는 기존 기능에서 강력한 최신 AEM 서비스로 전환하는 것을 돕기 위함입니다. 이들 기능은 구성, 구성 인식 및 확장이 가능합니다. 또한 사용자 지정 구성 요소를 표준화된 핵심 구성 요소 세트로 대체하여 개발을 가속화하고 애플리케이션 유지 관리 비용을 절감할 수 있습니다."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="구성 요소 변환기"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-core-components/using/introduction" text="핵심 구성 요소"

* [AEM 현대화 도구 세트](https://opensource.adobe.com/aem-modernize-tools/)를 활용하여 AEM Sites 구현을 현대화하는 데 필요한 수고를 줄일 수 있습니다. 이들 도구에는 다음과 같은 변환 작업이 포함됩니다.
   * 클래식(ExtJS) 대화 상자를 코랄 대화 상자로 변환
   * 기초 구성 요소를 핵심 구성 요소로 변환
   * 정적 템플릿 및 열 제어를 편집 가능한 템플릿 및 반응형 격자로 변환
   * 디자인 및 디자인 대화 상자를 편집 가능한 템플릿 정책으로 변환
* 프로젝트의 사용자 지정 구성 요소 라이브러리를 검토하고 가능한 경우 표준화된 [핵심 구성 요소](https://experienceleague.adobe.com/ko/docs/experience-manager-core-components/using/introduction) 세트로 전환하면 개발을 가속화하고 애플리케이션 유지 관리 비용을 절감할 수 있습니다.
* 레거시 템플릿과 동일한 기능을 갖춘 콘텐츠 조각 모델을 생성하고 향후 콘텐츠 조각 생성 시 이들 모델을 사용하십시오. 자세한 내용은 [콘텐츠 조각 모델](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models)을 참조하십시오.
* CI/CD 파이프라인을 통해 Git에서 `I18n` 사전을 가져와야 합니다. [설명서](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
