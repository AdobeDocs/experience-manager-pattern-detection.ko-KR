---
title: URC
description: 패턴 감지기 코드 도움말 페이지
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 24%

---

# URC {#urc}

지원되지 않는 실행 모드 구성

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="지원되지 않는 실행 모드 구성"
>abstract="URC는 AEM as a Cloud Service에서 지원되지 않는 실행 모드 이름을 기반으로 하는 구성의 사용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="지원되는 실행 모드"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="실행 모드"

URC는 AEM as a Cloud Service에서 지원되지 않는 실행 모드 이름을 기반으로 하는 구성의 사용을 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 애플리케이션에서 사용되는 모든 실행 모드가 지원되는지 검토한 다음 이들이 실행 모드 해결 방법 지침을 따르도록 하는 것입니다"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="실행 모드 해결 방법 지침"

* AEM에서 다양한 모드를 as a Cloud Service으로 실행하기 위해 사용될 수 있는 이름들의 세트는 제한된다.
* 지원되지 않는 실행 모드 이름을 기반으로 하는 구성은 AEM as a Cloud Service에 배포할 때 영향을 주지 않습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 URC 위반이 AEM Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오. 또한 GitHub에서 URC 위반 사례를 검토하여 사용자 지정 실행 모드 기반 OSGi 구성을 AEM as a Cloud Service으로 호환되도록 업데이트하는 방법에 대해 알아보십시오."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="WKND 레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="URC 위반 사례 - GitHub"

* 이 구성의 사용을 검토하여 이 구성이 필요한지 확인하십시오.
* 지원되는 구성 중 하나를 사용하여 구성의 이름을 변경합니다 [실행 모드 이름](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) 팔로우 [실행 모드 해결 방법 지침](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* [WKND 레거시 프로젝트](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc)를 검토한 다음 [URC 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc)을 수정하여 AEM as a Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오.
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
