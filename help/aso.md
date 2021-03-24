---
title: ASO
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 4%

---


# ASO {#aso}

AEM 시스템 개요

## 배경 {#background}

`ASO` AEM 인스턴스에 대한 일반 정보를 식별합니다. 각 검색 결과는 특정 시스템 정보 유형의 값 하나를 제공합니다.

하위 유형은 서로 다른 유형의 정보를 식별하는 데 사용됩니다.

* `aem.version`:AEM 버전.
* `aem.product`:AEM 제품 사용 감지(커머스, Forms 등)
* `node.count`:특정 유형의 대략적인 노드 수(페이지, 자산 등)
* `node.store`:노드 저장소 구현 유형(SegmentNodeStore, DocumentNodeStore).
* `data.store`:데이터 저장소 구현 유형(FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`:유지 관리 작업입니다.
* `slow.query`:느린 쿼리입니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* AEM 버전, 노드 수 및 노드 저장소 및 데이터 저장소 구현 유형은 정보용으로 제공됩니다.
* 사용자 정의 응용 프로그램은 Cloud Service으로 AEM에서 사용할 수 없는 제품 또는 기능에 의존할 수 있습니다.
* 지원되지 않는 기능으로 업그레이드하면 업그레이드에 실패하거나 작동하지 않는 응용 프로그램이 발생할 수 있습니다.

## 가능한 솔루션 {#solutions}

* 지원되지 않는 제품 또는 기능이 있는 AEM 업그레이드는 권장되지 않으며 지원되지 않을 수 있습니다.
* AEM의 최신 변경 사항을 Cloud Service으로 확인하려면 [릴리스 노트](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html)를 검토하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
