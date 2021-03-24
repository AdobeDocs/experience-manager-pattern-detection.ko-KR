---
title: OID
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# OID {#oid}

Oak 색인 정의

## 배경 {#background}

`OID` 은 Oak 색인 정의와 관련된 문제를 식별합니다. 표준 Oak 색인 정의에 수행된 수정을 식별합니다. 또한 AEM과 호환되지 않는 사용자 정의 Oak 색인 정의를 Cloud Service으로 식별합니다. 각 `OID` 검색에 대한 메시지는 인덱스를 식별하고 추가 정보를 제공합니다.

하위 유형은 서로 다른 유형의 정보를 식별하는 데 사용됩니다.

* `custom.index.violation`:사용자 지정 Oak 색인이 Cloud Service으로 AEM과 호환되지 않습니다.
* `standard.index.modification`:표준 Oak 색인을 수정합니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 표준 Oak 색인 정의에 대한 수정 사항은 AEM 업그레이드 중에 손실될 수 있습니다.
* oak 정의는 변경할 수 없으며, 고객 프로젝트 코드와 함께 패키징해야 하며, Cloud Manager를 통해서만 배포해야 합니다.
* 모든 Oak 색인 정의는 AEM의 Oak 인덱스에 대한 이름 지정 규칙 및 기타 규칙을 Cloud Service으로 따라야 합니다. 원치 않는 행동을 유발할 수 없는 행동.

## 가능한 솔루션 {#solutions}

* 메시지에 식별된 색인 규칙 위반을 해결합니다.
* 새 또는 사용자 정의 Oak 색인 정의를 배포하려면 Cloud Service [패키징 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html)으로 AEM을 따르십시오.
* 사용자 정의된 AEM 표준 인덱스와 새 사용자 정의 Oak 색인 정의는 AEM의 경우 [컨텐츠 인덱싱 지침](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition)을 Cloud Service으로 따라야 합니다.
* [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) 프로젝트를 검토하고 [OID 위반](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid)을 수정하여 Cloud Service과 호환되는 방법을 파악합니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
* [색인 변환기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools)를 활용하여 기존 사용자 지정 Oak 색인 정의를 Cloud Service 호환 Custom Oak 색인 정의로 AEM에 마이그레이션합니다.
