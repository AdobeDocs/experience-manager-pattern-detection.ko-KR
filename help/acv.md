---
title: ACV
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: d61fbb28fdf91fd9b356654d5cd2d50b156398c4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# ACV {#acv}

Assets Content Validator

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV는 자산 컨텐츠에서 누락된 필수 노드를 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="주목할 만한 변경 사항 - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR" text="Experience Manager as a Cloud Service - 릴리스 노트"

`ACV`  Assets의 Content Validator가 자산 컨텐츠에서 누락된 필수 노드를 식별합니다. 이로 인해 Experience Manager의 특정 Cloud Service 기능이 실패할 수 있습니다.

하위 유형은 다음과 같이 다양한 유형의 정보를 식별하는 데 사용됩니다.

* `assets.sanity.missing.jcrcontent`:저장소에서 필수 노드가 누락된 폴더를 식별합니다. 저장소에서 누락된 콘텐츠를 식별하면 끊어진 기능 또는 사용 사례를 방지할 수 있습니다.

## 가능한 의미와 위험 {#implications-and-risks}

이로 인해 Experience Manager에서 Cloud Service으로 상속된 속성에 의존하는 특정 자산 기능이 실패할 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="구현 지침"
>abstract="Adobe은 상속된 속성에 의존하는 끊어진 워크플로우를 방지하기 위해 컨텐츠 구조를 검토하도록 권장합니다. 도움이 필요하면 고객 지원팀에 문의하십시오."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 누락된 하위 노드가 있는 폴더를 분석합니다. 폴더 수를 관리할 수 있으면 수동으로 노드를 만들고, 그렇지 않으면 스크립트를 사용합니다.
* 명확히 하거나 문제를 해결하려면 [Experience Manager 고객 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
