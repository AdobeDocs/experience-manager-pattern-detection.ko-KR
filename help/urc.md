---
title: URC
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# URC {#urc}

지원되지 않는 실행 모드 구성

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="지원되지 않는 실행 모드 구성"
>abstract="URC는 AEM에서 Cloud Service으로 지원되지 않는 런타임 모드 이름을 기반으로 하는 구성 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="지원되는 실행 모드"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="런타임 모드"

`URC` 는 AEM에서 Cloud Service으로 지원되지 않는 런타임 모드 이름을 기반으로 하는 구성 사용을 식별합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 응용 프로그램에 사용된 모든 실행 모드가 지원되는지 검토하고 실행 모드 해결 지침을 따르는지 확인하는 것입니다"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="런타임 모드 해상도 지침"

* AEM as a Cloud Service에서 실행 모드에 사용할 수 있는 이름 집합은 제한됩니다.
* 지원되지 않는 런타임 모드 이름을 기반으로 하는 구성은 Cloud Service으로 AEM에 배포될 때 영향을 주지 않습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="도구 및 리소스"
>abstract="WKND-legacy 프로젝트를 검토하여 URC 위반을 AEM Cloud Service과 호환하는 방법을 이해합니다. 또한 Github의 URC 위반 예제를 검토하여 AEM을 Cloud Service으로 준수하도록 사용자 지정 실행 모드 기반 OSGi 구성을 업데이트하는 방법을 이해합니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND-이전 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="URC 위반 예 - Github"

* 이 구성의 사용 여부를 검토하여 필요한 경우 확인합니다.
* 지원되는 [실행 모드 이름](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) 중 하나를 사용하도록 구성 이름을 변경하고 [실행 모드 해상도 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution)을 따릅니다.
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) 프로젝트를 검토하고 [URC 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc)을 수정하고 Cloud Service으로 AEM과 호환되는 방법을 이해합니다.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
