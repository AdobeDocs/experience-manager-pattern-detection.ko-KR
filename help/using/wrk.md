---
title: WRK
description: 패턴 감지기 코드 도움말 페이지
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 92%

---

# WRK {#wrk}

워크플로

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="워크플로"
>abstract="WRK 코드는 워크플로 모델 또는 런처 관련 검색 결과를 식별합니다. AEM as a Cloud Service로 업그레이드할 때 사용자 지정 에셋 워크플로 모델을 마이그레이션하기 위해 보고됩니다. 이제 AEM as a Cloud Service를 통해 에셋 마이크로서비스에서 에셋 처리를 수행합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="에셋 마이크로서비스"

`WRK`는 워크플로 모델 또는 런처 관련 검색 결과를 식별합니다. AEM as a Cloud Service로 업그레이드할 때 사용자 지정 에셋 워크플로 모델을 마이그레이션하기 위해 보고됩니다.

현재 감지되는 워크플로 문제를 식별하기 위해 하위 유형이 사용됩니다.

* `custom.asset.workflow`: 사용자 지정 에셋 워크플로 모델 또는 런처 감지

## 가능한 영향 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="구현 지침"
>abstract="에셋 마이크로서비스에서 표준 에셋 워크플로를 자동으로 지원하므로, 가장 좋은 방법은 모든 사용자 지정 에셋 워크플로 모델 또는 런처를 검토하여 AEM as a Cloud Service로 전환할 때 이들이 필요한지 확인하는 것입니다. 에셋 워크플로를 맞춤화하려면 AEM as a Cloud Service와 호환되도록 에셋 워크플로 마이그레이션 도구를 통해 마이그레이션해야 합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="시작하기 - 에셋 마이크로서비스"

* 에셋 처리는 전통적으로 AEM 작성자 인스턴스에서 실행되는 에셋 워크플로를 통해 수행되었습니다. 이제 AEM as a Cloud Service를 통해 에셋 마이크로서비스에서 에셋 처리를 수행합니다. 다음을 참조하십시오. [에셋 마이크로서비스 개요](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) 추가 정보.
* 에셋 마이크로서비스는 표준 에셋 워크플로를 자동으로 지원합니다.
* 에셋 워크플로를 맞춤화하려면 AEM as a Cloud Service와 호환되도록 마이그레이션해야 합니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="도구 및 리소스"
>abstract="사용자 지정 에셋 워크플로 모델 또는 런처가 식별되면 에셋 워크플로 마이그레이션 도구 실행을 검토 및 계획하십시오. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="에셋 워크플로 마이그레이션 도구"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 사용자 지정 에셋 워크플로 모델 또는 런처가 식별되면 [에셋 워크플로 마이그레이션 도구](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html) 실행을 검토 및 계획하십시오.
* 자세한 내용은 [에셋 마이크로서비스 사용 시작하기](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html)를 참조하십시오.
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
