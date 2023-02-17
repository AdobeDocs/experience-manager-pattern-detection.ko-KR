---
title: ACV
description: 패턴 감지기 코드 도움말 페이지
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 0a6b0f8f2b64bf1c966b8f282a2205f2772afe3f
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 86%

---

# ACV {#acv}

Assets 콘텐츠 유효성 검사기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets 콘텐츠 유효성 검사기"
>abstract="ACV는 에셋 콘텐츠의 누락된 필수 노드를 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="주요 변경 내용 - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="Experience Manager as a Cloud Service - 릴리스 정보"

`ACV`  Assets Content Validator는 에셋 콘텐츠에서 누락된 필수 노드 및 위반 사항을 식별합니다. 이로 인해 Experience Manager as a Cloud Service의 특정 Assets 기능이 작동하지 않을 수 있습니다.

다양한 유형의 정보 식별을 위해 다음과 같은 하위 유형이 사용됩니다.

* `missing.jcrcontent`: 저장소에서 누락된 필수 노드가 포함된 폴더를 식별합니다. 저장소에서 누락된 콘텐츠를 식별하면 기능 또는 사용 사례가 끊어지는 것을 방지할 수 있습니다.
* `missing.original.rendition`: 저장소에서 누락된 필수 원본 렌디션이 포함된 에셋을 식별합니다. PDF의 페이지 미리보기는 AEMaaCS에서 하위 에셋을 생성할 필요가 없다는 점을 참고하십시오. 따라서 PDF 에셋의 경우 원본 렌디션이 누락된 하위 에셋 보고가 억제됩니다.
* `metadata.descendants.violation`: 저장소에 있는 에셋의 메타데이터 노드 아래에서 하위 항목이 100개를 초과하는 에셋을 식별합니다.
* `conflict.node`: /content/dam/ 경로 아래의 저장소에서 충돌 노드가 있는지 확인합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 이로 인해 상속된 속성에 의존하는 Experience Manager as a Cloud Service의 특정 Assets 기능이 작동하지 않을 수 있습니다.
* AEM Assets는 원본 렌디션의 존재 여부에 좌우됩니다. 원본 렌디션이 누락된 경우 Cloud Service에서 처리되는 에셋은 루프로 이동합니다. 하위 에셋 생성은 AEMaaCS에서 지원되지 않습니다.
* 메타데이터 노드 아래에 하위 항목이 많으면 이를 위반하는 에셋으로 구성된 폴더의 로드 속도가 느려질 수 있습니다.
* 충돌 노드가 있으면 AEM as a Cloud Service에서 수집 오류가 발생할 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="구현 지침"
>abstract="Adobe는 콘텐츠 구조를 검토하여 상속된 속성에 의존하는 워크플로가 끊어지는 것을 방지할 것을 권장합니다. 도움이 필요한 경우 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 누락된 하위 노드가 있는 경우 폴더를 분석하십시오. 폴더 수가 관리 가능한 경우 수동으로 노드를 생성하고, 그렇지 않은 경우 스크립트를 사용하십시오.
* 원본 렌디션이 누락된 에셋의 경우 에셋을 다시 업로드하거나 마이그레이션하기 전에 에셋을 삭제하십시오.
* 누락된 하위 에셋 원본 렌디션에 대해서는 조치가 필요하지 않습니다.
* 충돌 노드의 경우 해결해야 하거나 AEM as a Cloud Service으로 마이그레이션하기 전에 삭제해야 할 수 있습니다.
* 자세한 설명이 필요하거나 문제를 해결하려면 [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
