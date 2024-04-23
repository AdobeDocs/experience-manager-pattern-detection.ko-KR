---
title: ACV
description: 패턴 감지기 코드 도움말 페이지
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 70%

---

# ACV {#acv}

Assets 콘텐츠 유효성 검사기

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets 콘텐츠 유효성 검사기"
>abstract="ACV는 자산 콘텐츠의 누락된 필수 노드를 식별합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview" text="주요 변경 내용 - Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Experience Manager as a Cloud Service - 릴리스 정보"

ACV Assets Content Validator는 에셋 콘텐츠에서 누락된 필수 노드 및 위반 사항을 식별합니다. 이로 인해 Experience Manager as a Cloud Service의 특정 Assets 기능이 작동하지 않을 수 있습니다.

다양한 유형의 정보 식별을 위해 다음과 같은 하위 유형이 사용됩니다.

* `missing.jcrcontent`: 저장소에서 누락된 필수 노드가 포함된 폴더를 식별합니다. 저장소에서 누락된 콘텐츠를 식별하면 기능 또는 사용 사례가 끊어지는 것을 방지할 수 있습니다.
* `missing.original.rendition`: 저장소에서 누락된 필수 원본 렌디션이 포함된 자산을 식별합니다. PDF의 페이지 미리보기는 AEMaaCS에서 하위 자산을 생성할 필요가 없다는 점을 참고하십시오. 따라서 PDF 자산의 경우 원본 렌디션이 누락된 하위 자산 보고가 억제됩니다.
* `metadata.descendants.violation`: 저장소에 있는 자산의 메타데이터 노드 아래에서 하위 항목이 100개를 초과하는 자산을 식별합니다.
* `conflict.node`: /content/dam/ 경로 아래의 저장소에 충돌 노드가 있는지 식별합니다.
* `psb.file.large`: 크기가 2GB보다 큰 큰 PSB 파일(dc:format : application/vnd.3gpp.pic-bw-small)을 식별합니다.
* `invalid.asset.name`: 이름에 잘못된 문자[* / : [\] | # % { } ? &amp;]가 있는 자산을 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 이로 인해 상속된 속성에 의존하는 Experience Manager as a Cloud Service의 특정 Assets 기능이 작동하지 않을 수 있습니다.
* AEM Assets는 원본 렌디션의 존재 여부에 좌우됩니다. 원본 렌디션이 누락된 경우 Cloud Service의 에셋 처리가 루프로 이동합니다. 하위 자산 생성은 AEMaaCS에서 지원되지 않습니다.
* 메타데이터 노드 아래에 하위 항목이 많으면 이를 위반하는 에셋으로 구성된 폴더의 다운로드가 느려질 수 있습니다.
* 충돌 노드가 있으면 AEM as a Cloud Service에서 수집 실패가 발생할 수 있습니다.
* Experience Manager이 고해상도 PSB 파일을 처리할 수 없습니다. 대용량 파일을 처리하기 위해 ImageMagick을 사용하는 고객은 Experience Manager 서버를 적절하게 벤치마킹하지 않으면 성능에 영향을 받을 수 있습니다.
* 자산 이름에 잘못된 문자가 있으면 AEM as a Cloud Service로 마이그레이션하는 동안 오류가 발생할 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="구현 지침"
>abstract="Adobe은 콘텐츠 구조를 검토하여 상속된 속성에 의존하는 워크플로가 끊어지는 것을 방지할 것을 권장합니다. 도움이 필요한 경우 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 누락된 하위 노드가 있는 경우 폴더를 분석하십시오. 폴더 수가 관리 가능한 경우 수동으로 노드를 생성하고, 그렇지 않은 경우 스크립트를 사용하십시오.
* 원본 렌디션이 누락된 자산의 경우 자산을 다시 업로드하거나 마이그레이션하기 전에 자산을 삭제하십시오.
* 누락된 하위 자산 원본 렌디션에 대해서는 조치가 필요하지 않습니다.
* 충돌 노드가 있는 경우 AEM as a Cloud Service으로 마이그레이션하기 전에 해결하거나 삭제해야 합니다.
* 여러 개의 대용량 PSD 또는 PSB 파일을 처리하려면 Adobe 고객 지원 센터에 문의하십시오. Experience Manager은 30000 x 23000 픽셀보다 큰 고해상도 PSB 파일을 처리하지 못할 수 있습니다. 다음을 참조하십시오 [설명서](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/extending/best-practices-for-imagemagick).
* 다음으로 문의: [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명 또는 문제 해결을 위해.
