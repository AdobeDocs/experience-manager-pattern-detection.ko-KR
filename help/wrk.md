---
title: 작업
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# 작업 {#wrk}

워크플로우

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="워크플로우"
>abstract="WRK 코드는 워크플로우 모델 또는 실행 프로그램과 관련된 검색 결과를 식별합니다. 이는 AEM으로 Cloud Service으로 업그레이드할 때 사용자 지정 자산 워크플로우 모델을 마이그레이션해야 하기 때문에 보고됩니다. 이제 AEM을 Cloud Service으로 사용하여 자산 처리가 자산 마이크로서비스에 의해 수행됩니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="자산 마이크로서비스"

`WRK` 워크플로우 모델 또는 런처 와 관련된 검색 결과를 식별합니다. 이는 AEM으로 Cloud Service으로 업그레이드할 때 사용자 지정 자산 워크플로우 모델을 마이그레이션해야 하기 때문에 보고됩니다.

현재 감지된 워크플로우 문제 유형을 식별하는 데 하위 유형이 사용됩니다.

* `custom.asset.workflow`:사용자 지정 자산 워크플로우 모델 또는 런처 탐지

## 가능한 의미 및 위험 {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="구현 지침"
>abstract="표준 자산 워크플로우가 내 자산 마이크로서비스에서 자동으로 지원되므로, 우수 사례는 모든 사용자 지정 자산 워크플로우 모델 또는 런처를 검토하여 AEM으로 전환한 후 이 워크플로우가 필요한지 확인하는 것입니다. 자산 워크플로우 마이그레이션 도구의 도움으로 AEM as a Cloud Service에서 작업하려면 자산 워크플로우를 사용자 지정하려면 마이그레이션이 필요합니다"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="시작하기 - 자산 마이크로서비스"

* 일반적으로 자산 처리는 AEM 작성자 인스턴스에서 실행되는 자산 워크플로우를 사용하여 수행되었습니다. 이제 AEM을 Cloud Service으로 사용하여 자산 처리가 자산 마이크로서비스에 의해 수행됩니다. 자세한 내용은 [자산 마이크로서비스 개요](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html)를 참조하십시오.
* 표준 자산 워크플로우는 내 자산 마이크로서비스에서 자동으로 지원됩니다.
* AEM as a Cloud Service에서 작업하려면 자산 워크플로우에 대한 사용자 지정에서 마이그레이션이 필요합니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="도구 및 리소스"
>abstract="사용자 지정 자산 워크플로우 모델 또는 런처가 식별되면 자산 워크플로우 마이그레이션 도구를 실행하고 검토 및 계획합니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="자산 워크플로우 마이그레이션 도구"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 사용자 지정 자산 워크플로우 모델 또는 런처가 식별되는 경우 [자산 워크플로우 마이그레이션 도구](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html)를 실행할 계획입니다.
* 자세한 내용은 [자산 마이크로서비스 사용 시작](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html)을 검토하십시오.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
