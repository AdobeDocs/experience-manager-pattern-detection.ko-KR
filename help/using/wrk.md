---
title: WRK
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: ht
source-wordcount: '325'
ht-degree: 100%

---

# WRK {#wrk}

워크플로

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="워크플로"
>abstract="WRK 코드는 워크플로 모델 또는 시작 관리자 관련 검색 결과를 식별합니다. 이러한 식별은 AEM as a Cloud Service로 업그레이드할 때 사용자 정의 자산 워크플로 모델을 마이그레이션하기 위해 보고됩니다. AEM as a Cloud Service를 통해 자산 마이크로서비스에서 자산 처리를 수행합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="자산 마이크로서비스"

`WRK`는 워크플로 모델 또는 시작 관리자 관련 검색 결과를 식별합니다. 이러한 식별은 AEM as a Cloud Service로 업그레이드할 때 사용자 정의 자산 워크플로 모델을 마이그레이션하기 위해 보고됩니다.

현재 감지되는 워크플로 문제를 식별하기 위해 하위 유형이 사용됩니다.

* `custom.asset.workflow`: 사용자 정의 자산 워크플로 모델 또는 시작 관리자 감지

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="구현 지침"
>abstract="자산 마이크로서비스는 표준 자산 워크플로를 자동으로 지원합니다. 따라서 모범 사례는 모든 사용자 정의 자산 워크플로 모델 또는 시작 관리자를 검토하는 것입니다. 검토할 때 AEM as a Cloud Service로 전환한 후에 필요한지 여부를 확인할 수 있습니다. 자산 워크플로를 맞춤화하려면 AEM as a Cloud Service와 호환되도록 자산 워크플로 마이그레이션 도구를 통해 마이그레이션해야 합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="시작하기 - 자산 마이크로서비스"

* 자산 처리는 전통적으로 AEM 작성자 인스턴스에서 실행되는 자산 워크플로를 통해 수행되었습니다. AEM as a Cloud Service를 통해 자산 마이크로서비스에서 자산 처리를 수행합니다. 자세한 내용은 [자산 마이크로서비스 개요](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview)를 참조하십시오.
* 자산 마이크로서비스는 표준 자산 워크플로를 자동으로 지원합니다.
* 자산 워크플로를 맞춤화하려면 AEM as a Cloud Service와 호환되도록 마이그레이션해야 합니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="도구 및 리소스"
>abstract="사용자 정의 자산 워크플로 모델 또는 시작 관리자가 식별되면 자산 워크플로 마이그레이션 도구 실행을 검토 및 계획하십시오. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="자산 워크플로 마이그레이션 도구"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 사용자 정의 자산 워크플로 모델 또는 시작 관리자가 식별되면 [자산 워크플로 마이그레이션 도구](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool) 실행을 검토 및 계획하십시오.
* 자세한 내용은 [자산 마이크로서비스 사용 시작하기](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use)를 참조하십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
