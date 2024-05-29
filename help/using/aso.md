---
title: ASO
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: ht
source-wordcount: '475'
ht-degree: 100%

---

# ASO {#aso}

AEM 시스템 개요

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM 시스템 개요"
>abstract="ASO 코드는 AEM 인스턴스에 대한 일반 정보를 식별합니다. 각각의 결과는 마이그레이션 계획 수립 및 리팩터링에 도움이 되는 특정 유형의 시스템 정보 중 하나의 값을 제공합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - 릴리스 정보"

`ASO`는 AEM 인스턴스에 대한 일반 정보를 식별합니다. 각각의 결과는 특정 유형의 시스템 정보 중 하나의 값을 제공합니다.

다양한 유형의 정보를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.

* `aem.version`: AEM 버전
* `aem.product`: AEM 제품(Commerce, Forms 등)의 사용을 감지합니다.
* `node.count`: 특정 유형(페이지, 자산 등)의 대략적인 노드 수 및 노드의 총계입니다.
* `node.store`: 노드 저장소 구현 유형(SegmentNodeStore, DocumentNodeStore) 및 크기
* `data.store`: 데이터 저장소 구현 유형(FileDataStore, S3DataStore, AzureDataStore)
* `maintenance.task`: 유지 관리 작업
* `slow.query`: 느린 쿼리
* `group.membership`: 그룹 내 사용자 및 하위 그룹(직접 선언된 멤버만 해당)의 수입니다.
* `cqtag.count`: CQ 태그가 지정된 자산 수
* `smarttag.count`: 스마트 태그가 지정된 자산 수
* `ccom.version`: 핵심 구성 요소 패키지 버전
* `instance.type`: AEM 인스턴스 유형(작성자/게시)
* `unprocessed.asset.count`: 처리되지 않은 자산 수
* `vanity.url.count`: vanity URL 수
* `index.size`: 총 마이그레이션 가능한 Lucene 인덱스 크기입니다.
* `workflow.count`: 실행 중이고 오래된 상태의 작성자 워크플로 수입니다.
* `jvm.arguments`: AEM을 시작할 때 명령줄에 추가되는 JVM 인수입니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* AEM 버전, 노드 수, 그룹 멤버십, 노드 저장소, 데이터 저장소 구현 유형, CQ 태그 수, 스마트 태그 수, 핵심 구성 요소 버전, AEM 인스턴스 유형과 처리되지 않은 자산 수가 정보 제공을 목적으로 제공됩니다.
* Vanity URL의 수가 많을수록(1,000개 초과) Dispatcher 및 게시 서버에 고가의 쿼리가 있는 로드가 발생할 수 있습니다.
* 맞춤형 애플리케이션은 AEM as a Cloud Service에서 사용할 수 없는 제품 및 기능에 의존할 수 있습니다.
* 지원되지 않는 기능을 업그레이드하면 업그레이드 실패 및 애플리케이션 오작동을 야기할 수 있습니다.
* 실행 중이거나 오래된 상태의 작성자 워크플로가 많으면 성능이 저하될 수 있습니다.
* 느린 쿼리는 시스템 성능을 저하시킬 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="구현 지침"
>abstract="ASO 코드를 통해 노출되는 정보는 버전, 제품 추가 기능 및 시스템 수준 정보 등 AEM 환경에 대한 일반 정보를 제공합니다. AEM as a Cloud Service에서 지원되지 않는 제품이나 기능이 있는지 검토하십시오. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 지원되지 않는 제품이나 기능을 통해 AEM을 업그레이드하는 방법은 권장되지 않으며 이러한 기능은 지원되지 않을 수 있습니다.
* 처리되지 않은 자산은 처리되어야 하며, 자산 `jcr:content` 노드의 `dam:assetState` 속성은 “처리됨”으로 설정되어야 합니다. 또는 AEMaaCS로 마이그레이션하기 전에 마이그레이션 세트에서 이러한 자산을 제거해야 합니다.
* Vanity URL은 Apache Rewrite로 대체할 수 있습니다.
* 느린 쿼리에 대한 문제 해결 방법은 [설명서](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/implementing/developing/bestpractices/troubleshooting-slow-queries)를 참조하십시오.
* AEM as a Cloud Service의 최신 변경 내용에 대해 자세히 알아보려면 [릴리스 정보](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current)를 확인하십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
