---
title: INST
description: 패턴 감지기 코드 도움말 페이지
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 76%

---

# INST {#inst}

설치된 아티팩트

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="설치된 아티팩트"
>abstract="INST는 고객이 AEM에 설치한 맞춤형/서드파티 패키지 및 번들을 식별합니다. 이들을 보고하면 일반적인 업그레이드 범위 내에서 시스템 상태를 특성화하는 데 도움이 됩니다. 모든 서드파티 패키지는 AEM as a Cloud Service 개발 및 패키징 지침을 준수해야 합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="개발 지침 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="패키징 지침 - AEM as a Cloud Service"

INST는 고객이 AEM에 설치한 맞춤형/서드파티 패키지 및 번들을 식별합니다. 이들을 보고하면 일반적인 업그레이드 범위 내에서 시스템 상태를 특성화하는 데 도움이 됩니다.

여러 버전의 패키지를 설치한 경우 최신 버전만 보고됩니다.

감지된 패키지 및 번들은 반드시 AEM as a Cloud Service에 최적화되어 있지는 않습니다. 제작자 또는 Adobe를 통해 서드파티 패키지와 AEM as a Cloud Service의 호환성을 확인해야 합니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `custom.bundle`: AEM에 설치된 번들
* `custom.package`: AEM에 설치된 패키지

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="구현 지침"
>abstract="고객은 더 이상 CRX 패키지 관리자를 사용하여 서드파티 패키지를 설치할 수 없습니다. 고객은 구조화해야 하는 이러한 설치된 아티팩트를 검토하고 AEM에서 as a Cloud Service으로 작동하도록 최적화해야 합니다. AEMas a Cloud Service 와의 호환성을 위해 작성자 또는 Adobe과 함께 서드파티 패키지를 확인합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="컨테이너 패키지에 하위 패키지 임베드"


* AEM as a Cloud Service에서는 CRX 패키지 관리자를 사용하여 서드파티 패키지를 설치할 수 없습니다.
* 서드파티 패키지에 의존하는 애플리케이션은 AEM as a Cloud Service와 호환되도록 올바르게 배포되지 않으면 예상대로 작동하지 않을 수 있습니다.
* AEM as a Cloud service에 최적화하지 않은 서드파티 공급업체 패키지를 사용하면 원하지 않은 비헤이비어가 발생할 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 INST 위반이 AEM Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오. 또한 GitHub에서 INST 위반 사례를 검토하여 이 문제를 해결하고 AEM에서 as a Cloud Service으로 배포하는 방법에 대해 알아보십시오."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="WKND 레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="INST 위반 사례 - GitHub"

* 서드파티 패키지는 Cloud Manager [배포 프로세스](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process)를 사용하여 AEM에 프로젝트의 일부로 배포해야 합니다.
* AEM as a Cloud Service용 프로젝트에 [서드파티 패키지를 임베드](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages)하는 방법을 확인하십시오.
* 모든 서드파티 패키지는 AEM as a Cloud Service [개발](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) 및 [패키징](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) 지침을 준수해야 합니다.
* [WKND 레거시](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) 프로젝트를 검토한 다음 [INST 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst)을 수정하여 AEM as a Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오.
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
