---
title: INST
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# INST {#inst}

설치된 객체

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="설치된 객체"
>abstract="INST는 고객이 AEM에 설치한 사용자 정의 및 제3자 패키지 및 번들을 식별합니다. 이러한 내용은 시스템 상태를 업그레이드 노력의 일반적인 범위라고 설명하는 데 도움이 되는 것으로 보고됩니다. 제3자 패키지는 Cloud Service 개발 및 패키징 지침으로서 AEM을 준수해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="개발 지침 - Cloud Service의 AEM"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html" text="패키징 지침 - Cloud Service으로 AEM"

`INST` 고객이 AEM에 설치한 사용자 지정 및 제3자 패키지 및 번들을 식별합니다. 이러한 내용은 시스템 상태를 업그레이드 노력의 일반적인 범위라고 설명하는 데 도움이 되는 것으로 보고됩니다.

패키지의 여러 버전이 설치되면 최신 버전만 보고됩니다.

검색된 패키지와 번들이 Cloud Service으로 AEM에 최적화되지 않을 수 있습니다. 모든 제3자 패키지는 AEM과 Cloud Service의 호환성을 위해 작성자 또는 Adobe과 함께 확인되어야 합니다.

하위 유형은 서로 다른 유형의 정보를 식별하는 데 사용됩니다.

* `custom.bundle`:AEM에 설치된 번들.
* `custom.package`:AEM에 설치된 패키지입니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="구현 지침"
>abstract="고객은 CRX 패키지 관리자를 사용하여 더 이상 타사 패키지를 설치할 수 없습니다. 고객은 설치된 이러한 결함을 검토하여 AEM에서 Cloud Service으로 작동하도록 구성하고 최적화해야 합니다. 모든 제3자 패키지는 AEM과 Cloud Service의 호환성을 위해 작성자 또는 Adobe과 함께 확인되어야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embeddeds" text="컨테이너 패키지에 하위 패키지 포함"


* AEM에서는 CRX 패키지 관리자를 사용하여 타사 패키지를 Cloud Service으로 설치할 수 없습니다.
* 제3자 패키지에 의존하는 응용 프로그램은 Cloud Service으로 AEM에서 올바르게 배포되기 전까지 예상대로 작동하지 않을 수 있습니다.
* AEM에 대해 클라우드 서비스로 최적화되지 않은 경우 타사 공급업체 패키지로 인해 원치 않는 동작이 발생할 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 INST 위반 사항이 AEM Cloud Service과 호환되도록 하는 방법을 파악하십시오. 또한 Github에서 INST 위반 사례를 검토하여 Cloud Service으로 수정 및 배포할 수 있는 방법을 이해합니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND-레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="INST 위반 예 - Github"

* 타사 패키지는 클라우드 관리자 [배포 프로세스](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process)를 사용하여 프로젝트의 일부로 AEM에 배포되어야 합니다.
* AEM용 프로젝트에서 Cloud Service으로 [타사 패키지](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages)를 포함하는 방법을 검토합니다.
* 타사 패키지는 Cloud Service [개발](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) 및 [패키징](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html) 지침으로 AEM을 준수해야 합니다.
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) 프로젝트를 검토하고 [INST 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst)을 수정하여 Cloud Service과 호환되는 방법을 파악합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
