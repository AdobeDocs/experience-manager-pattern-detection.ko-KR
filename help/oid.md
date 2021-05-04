---
title: OID
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# OID {#oid}

Oak 색인 정의

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Oak 색인 정의"
>abstract="OID는 Oak 색인 정의와 관련된 문제를 식별합니다. 표준 Oak 색인 정의에 수행된 수정을 식별합니다. 또한 AEM과 호환되지 않는 사용자 정의 Oak 색인 정의를 Cloud Service으로 식별합니다. 각 OID 검색에 대한 메시지는 인덱스를 식별하고 추가 정보를 제공합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#how-to-use" text="콘텐츠 인덱싱 지침"

`OID` 은 Oak 색인 정의와 관련된 문제를 식별합니다. 표준 Oak 색인 정의에 수행된 수정을 식별합니다. 또한 AEM과 호환되지 않는 사용자 정의 Oak 색인 정의를 Cloud Service으로 식별합니다. 각 `OID` 검색에 대한 메시지는 인덱스를 식별하고 추가 정보를 제공합니다.

하위 유형은 서로 다른 유형의 정보를 식별하는 데 사용됩니다.

* `custom.index.violation`:사용자 지정 Oak 색인이 Cloud Service으로 AEM과 호환되지 않습니다.
* `standard.index.modification`:표준 Oak 색인을 수정합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 컨텐츠 인덱싱 지침에 따라 모든 사용자 정의 색인을 검토하고 제한하는 것입니다. 색인 변환기를 활용하여 기존 사용자 정의 Oak 색인 정의를 Cloud Service 호환 Custom Oak 색인 정의로 AEM에 마이그레이션"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#oak-indexes" text="패키징 지침"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="색인 변환기"

* 표준 Oak 색인 정의에 대한 수정 사항은 AEM 업그레이드 중에 손실될 수 있습니다.
* oak 정의는 변경할 수 없으며, 고객 프로젝트 코드와 함께 패키징해야 하며, Cloud Manager를 통해서만 배포해야 합니다.
* 모든 Oak 색인 정의는 AEM의 Oak 인덱스에 대한 이름 지정 규칙 및 기타 규칙을 Cloud Service으로 따라야 합니다. 원치 않는 행동을 유발할 수 없는 행동.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="도구 및 리소스"
>abstract="WKND 레거시 프로젝트를 검토하여 프로젝트에서 OID 위반을 해결할 수 있는 방법을 이해합니다. 또한 Github에서 OID 위반 예제를 검토하여 색인 변환기 도구를 사용하여 이전 인덱스를 변환하고 AEM과 Cloud Service으로 호환되는 방법을 확인합니다."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="WKND-레거시 프로젝트"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="OID 위반 예 - Github"

* 메시지에 식별된 색인 규칙 위반을 해결합니다.
* 새 또는 사용자 정의 Oak 색인 정의를 배포하려면 Cloud Service [패키징 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html)으로 AEM을 따르십시오.
* 사용자 정의된 AEM 표준 인덱스와 새 사용자 정의 Oak 색인 정의는 AEM의 경우 [컨텐츠 인덱싱 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition)을 Cloud Service으로 따라야 합니다.
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) 프로젝트를 검토하고 [OID 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid)을 수정하여 Cloud Service과 호환되는 방법을 파악합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
* [색인 변환기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools)를 활용하여 기존 사용자 지정 Oak 색인 정의를 Cloud Service 호환 Custom Oak 색인 정의로 AEM에 마이그레이션합니다.
