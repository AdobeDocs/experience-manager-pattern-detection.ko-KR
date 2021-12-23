---
title: ACV
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 301aef7e53e94eb5941691450b3f1192408f2c6b
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 2%

---

# ACV {#acv}

Assets Content Validator

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV는 자산 컨텐츠에서 누락된 필수 노드를 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="주요 변경 사항 - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR" text="Experience Manager as a Cloud Service - 릴리스 노트"

`ACV`  Assets의 Content Validator가 자산 컨텐츠에서 누락된 필수 노드를 식별합니다. 이로 인해 Experience Manager as a Cloud Service의 특정 자산 기능이 실패할 수 있습니다.

하위 유형은 다음과 같이 다양한 유형의 정보를 식별하는 데 사용됩니다.

* `missing.jcrcontent`: 저장소에서 필수 노드가 누락된 폴더를 식별합니다. 저장소에서 누락된 콘텐츠를 식별하면 끊어진 기능 또는 사용 사례를 방지할 수 있습니다.
* `missing.original.rendition`: 저장소에서 필수 원본 표현물이 누락된 자산을 식별합니다.

## 가능한 의미와 위험 {#implications-and-risks}

* 이로 인해 Experience Manager as a Cloud Service의 상속된 속성에 의존하는 특정 자산 기능이 실패할 수 있습니다.
* AEM Assets은 원본 표현물의 존재여부에 따라 다릅니다. 원래 표현물이 누락된 경우 Cloud Service의 자산 처리가 루프로 이동합니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="구현 지침"
>abstract="Adobe은 상속된 속성에 의존하는 끊어진 워크플로우를 방지하기 위해 컨텐츠 구조를 검토하도록 권장합니다. 도움이 필요하면 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 누락된 하위 노드가 있는 폴더를 분석합니다. 폴더 수를 관리할 수 있으면 수동으로 노드를 만들고, 그렇지 않으면 스크립트를 사용합니다.
* 자산에서 원래 표현물이 누락된 경우 마이그레이션하기 전에 자산을 다시 업로드하거나 삭제하십시오.
* 연락하여 [고객 지원 팀 Experience Manager](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) 명확히 하거나 문제를 해결하기 위해.
