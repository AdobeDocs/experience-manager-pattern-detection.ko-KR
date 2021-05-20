---
title: INST
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# INST {#inst}

설치된 아티팩트

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="설치된 아티팩트"
>abstract="INST는 고객이 AEM에 설치한 사용자 지정 및 타사 패키지 및 번들을 식별합니다. 이러한 정보는 시스템의 상태를 업그레이드 작업의 일반적인 범위로서 파악하는 데 도움이 되기 위해 보고됩니다. 모든 타사 패키지는 Cloud Service 개발 및 패키징 지침으로서 AEM을 준수해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="개발 지침 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html" text="패키징 지침 - AEM as a Cloud Service"

`INST` 고객이 AEM에 설치한 사용자 지정 및 타사 패키지 및 번들을 식별합니다. 이러한 정보는 시스템의 상태를 업그레이드 작업의 일반적인 범위로서 파악하는 데 도움이 되기 위해 보고됩니다.

여러 버전의 패키지가 설치되면 최신 버전만 보고됩니다.

감지된 패키지 및 번들은 AEM as a Cloud Service에 최적화되어 있지 않았습니다. 모든 타사 패키지는 AEM as a Cloud Service와의 호환성을 위해 작성자 또는 Adobe과 확인해야 합니다.

하위 유형은 다양한 유형의 정보를 식별하는 데 사용됩니다.

* `custom.bundle`:AEM에 설치된 번들입니다.
* `custom.package`:AEM에 설치된 패키지.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="구현 지침"
>abstract="고객은 CRX Package Manager 를 사용하여 더 이상 타사 패키지를 설치할 수 없습니다. 고객은 설치된 이러한 가공물을 검토하여 AEM as a Cloud Service으로 작동하도록 구조화하고 최적화해야 합니다. 모든 타사 패키지는 AEM as a Cloud Service와의 호환성을 위해 작성자 또는 Adobe과 확인해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embeddeds" text="컨테이너 패키지에 하위 패키지 포함"


* AEM에서 CRX Package Manager 를 Cloud Service으로 사용하여 타사 패키지를 설치할 수 없습니다.
* 타사 패키지에 종속된 애플리케이션은 Cloud Service으로 AEM에서 작동하도록 올바르게 배포될 때까지 제대로 작동하지 않을 수 있습니다.
* AEM as a Cloud Service에 최적화되지 않은 경우 타사 공급업체 패키지로 인해 원치 않는 동작이 발생할 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="도구 및 리소스"
>abstract="WKND-legacy 프로젝트를 검토하여 INST 위반을 AEM Cloud Service과 호환하는 방법을 이해합니다. 또한 Github에서 INST 위반 예를 검토하여 이 예제를 수정하고 AEM에서 Cloud Service으로 배포하는 방법을 이해합니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-이전 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="INST 위반 예 - Github"

* 타사 패키지는 Cloud Manager [배포 프로세스](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process)를 사용하여 프로젝트의 일부로 AEM에 배포해야 합니다.
* AEM용 프로젝트에 타사 패키지](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages)를 Cloud Service으로 포함하는 방법을 검토합니다.[
* 타사 패키지는 AEM을 Cloud Service [개발](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) 및 [패키징](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html) 지침으로 준수해야 합니다.
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) 프로젝트를 검토하고 [INST 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst)을 수정하고 AEM과 Cloud Service으로 호환되는 방법을 이해합니다.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
