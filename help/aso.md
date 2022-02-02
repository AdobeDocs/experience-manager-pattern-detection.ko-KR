---
title: ASO
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: d45c6b561a9665cbac39bfd8d9ce6eb2658c24e8
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 4%

---

# ASO {#aso}

AEM 시스템 개요

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM 시스템 개요"
>abstract="ASO 코드는 AEM 인스턴스에 대한 일반 정보를 식별합니다. 각 검색 결과는 마이그레이션 계획 및 리팩터링 작업에 도움이 될 수 있는 특정 유형의 시스템 정보에 대한 하나의 값을 제공합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - 릴리스 노트"

`ASO` AEM 인스턴스에 대한 일반 정보를 식별합니다. 각 검색 결과는 특정 유형의 시스템 정보에 하나의 값을 제공합니다.

하위 유형은 다양한 유형의 정보를 식별하는 데 사용됩니다.

* `aem.version`: AEM 버전입니다.
* `aem.product`: AEM 제품 사용 감지(상거래, Forms 등).
* `node.count`: 특정 유형의 대략적인 노드 수(페이지, 자산 등) 그리고 노드의 총 합계입니다.
* `node.store`: 노드 저장소 구현 유형(SegmentNodeStore, DocumentNodeStore) 및 그 크기입니다.
* `data.store`: 데이터 저장소 구현 유형(FileDataStore, S3DataStore, AzureDataStore)입니다.
* `maintenance.task`: 유지 관리 작업입니다.
* `slow.query`: 느린 쿼리
* `group.membership`: 그룹의 사용자 및 하위 그룹( 직접/선언된 멤버만) 수입니다.
* `cqtag.count`: CQ 태그가 지정된 자산 수입니다.
* `smarttag.count`: 스마트 태그가 지정된 자산 수입니다.
* `ccom.version`: 코어 구성 요소 패키지의 버전입니다.
* `instance.type`: AEM 인스턴스 유형(작성자|게시)입니다.

## 가능한 의미와 위험 {#implications-and-risks}

* AEM 버전, 노드 수, 그룹 멤버십, 노드 저장소, 데이터 저장소 구현 유형, CQ 태그 수, 스마트 태그 수, 코어 구성 요소 버전 및 AEM 인스턴스 유형이 정보용으로 제공됩니다.
* 사용자 지정 애플리케이션은 AEM as a Cloud Service에서 사용할 수 없는 제품이나 기능을 사용할 수 있습니다.
* 지원되지 않는 기능을 사용하여 업그레이드하면 업그레이드에 실패하고 작동하지 않는 응용 프로그램이 발생할 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="구현 지침"
>abstract="ASO 코드를 통해 노출된 정보는 버전, 제품 추가 기능, 시스템 수준 정보 등 AEM 환경에 대한 일반 정보를 제공하며 AEM as a Cloud Service에서 지원되지 않는 제품이나 기능에 대해 검토해야 합니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 지원되지 않는 제품이나 기능을 사용한 AEM 업그레이드는 권장되지 않으며 지원되지 않을 수 있습니다.
* 를 검토합니다. [릴리스 노트](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR) AEM as a Cloud Service의 최신 변경 사항에 대해 알아보십시오.
* 연락하여 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) 명확히 하거나 문제를 해결하기 위해.
