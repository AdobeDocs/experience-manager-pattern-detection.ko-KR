---
title: OID
description: 패턴 감지기 코드 도움말 페이지
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 48%

---

# OID {#oid}

Oak 색인 정의

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak 색인 정의"
>abstract="OID는 Oak 색인 정의와 관련된 문제를 식별합니다. 이는 표준 Oak 색인 정의에 대해 수정된 내용을 식별합니다. 또한 AEM as a Cloud Service와 호환되지 않는 사용자 지정 Oak 색인 정의를 식별합니다. 각 OID 검색 결과에 대한 메시지는 색인을 식별하며 추가 정보를 제공합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#how-to-use" text="콘텐츠 색인화 지침"

`OID`  Oak 색인 정의와 관련된 문제를 식별합니다. 이는 표준 Oak 색인 정의에 대해 수정된 내용을 식별합니다. 또한 AEM as a Cloud Service와 호환되지 않는 사용자 지정 Oak 색인 정의를 식별합니다. 각각에 대한 메시지 `OID` 찾기는 색인을 식별하며 추가 정보를 제공합니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `index.rule.violation`: 사용자 지정 Oak 색인과 AEM as a Cloud Service와의 비호환성
* `standard.index.modification`: 표준 Oak 색인의 수정 내용

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 모든 사용자 지정 색인을 검토하고 콘텐츠 색인화 지침에 따라 재구성하는 것입니다. AEM 인덱스 변환기를 사용하여 기존 사용자 지정 Oak 색인 정의를 as a Cloud Service으로 호환되는 사용자 지정 Oak 색인 정의로 마이그레이션하십시오"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#oak-indexes" text="패키징 지침"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools" text="인덱스 변환기"

* 표준 Oak 색인 정의에 대해 수정된 내용은 AEM 업그레이드 도중 손실될 수 있습니다.
* Oak 정의는 변경이 불가하고, 고객 프로젝트 코드로 패키징해야 하며, Cloud Manager를 통해서만 배포할 수 있습니다.
* 모든 Oak 색인 정의는 AEM as a Cloud Service으로 Oak 색인에 대한 이름 지정 규칙 및 기타 규칙을 따라야 합니다. 그렇지 않으면 원하지 않은 비헤이비어가 발생할 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 프로젝트에서 OID 위반을 해결하는 방법에 대해 알아보십시오. 또한 GitHub에서 OID 위반 사례를 검토하여 인덱스 변환기 도구를 사용하여 레거시 인덱스를 변환하고 AEM과 as a Cloud Service으로 호환되도록 하는 방법에 대해 알아보십시오."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND 레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="OID 위반 사례 - GitHub"

* 메시지에서 식별된 색인 규칙 위반을 해결하십시오.
* 새 Oak 색인 정의 또는 사용자 지정 Oak 색인 정의를 배포하려면 AEM as a Cloud Service을 따르십시오 [패키징 지침](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure).
* 맞춤화된 AEM 표준 색인 및 새로운 사용자 지정 Oak 색인 정의는 [콘텐츠 색인화 지침](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/indexing#preparing-the-new-index-definition) AEM용 as a Cloud Service.
* [WKND 레거시](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) 프로젝트를 검토한 다음 [OID 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid)을 수정하여 AEM as a Cloud Service와 호환되도록 하는 방법에 대해 알아보십시오.
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
* 사용 [인덱스 변환기](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/index-converter#refactoring-tools) 기존 사용자 지정 Oak 색인 정의를 AEMas a Cloud Service 와 호환되는 사용자 지정 Oak 색인 정의로 마이그레이션하려면 다음을 수행하십시오.
