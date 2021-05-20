---
title: URS
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# URS {#urs}

지원되지 않는 저장소 구조

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="지원되지 않는 저장소 구조"
>abstract="URS는 지원되지 않는 저장소 구조의 사례를 식별합니다. 이는 AEM 제품 코드와 고객 코드 간의 충돌, /etc에서 저장소의 다른 폴더로 재구성된 컨텐츠 등을 방지하기 위한 정보를 나타냅니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="저장소 구조 변경"

## 배경 {#background}

`URS` 지원되지 않는 저장소 구조의 사례를 식별합니다. AEM 6.4부터 저장소 컨텐츠 재구성에 대한 지침이 제공되었습니다. AEM 제품 코드와 고객 코드에 대한 계층을 명확히 설명하고 계층 간 충돌을 방지하여 컨텐츠가 `/etc`에서 리포지토리의 다른 폴더로 재구성되어 다음 고급 규칙을 따릅니다.

* AEM 제품 코드는 항상 `/libs`에 배치되며, 사용자 지정 코드는 `/apps`, `/content` 및 `/conf`에 삽입해야 합니다.
* AEM as a Cloud Service에 대해 이러한 지침을 따르는 것이 좋습니다.

하위 유형은 해결해야 하는 특정 유형의 저장소 문제를 식별하는 데 사용됩니다.
* `clientlibs.location`:경로별로 참조하 `/etc` 는 클라이언트 라이브러리.
* `file.location`:설치  `/etc` 후 수정된 아래의 파일입니다.
* `node.location`:설치  `/etc` 후 수정된 아래의 노드입니다.
* `workflow.location`:아래의 워크플로우 모델 또는 런처  `/etc/workflow`.
* `package.structure`:변경할 수 있는 컨텐츠와 변경할 수 없는 컨텐츠를 모두 포함하는 패키지입니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 이전 경로에 의존하는 사용자 지정 코드는 원치 않는 동작과 제품 기능에 영향을 줄 수 있습니다.
* 변경할 수 있는 컨텐츠와 변경할 수 없는 컨텐츠를 모두 포함하는 패키지는 배포 중에 문제를 일으킬 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 코드 프로젝트를 검토하고 AEM 프로젝트 구조 지침을 준수하고 AEM에서 Cloud Service으로 원치 않는 동작을 초래할 수 있는 오래된/지원되지 않는 저장소 경로에 코드를 의존하는 것을 피하는 것입니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="AEM 프로젝트 구조 지침"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* AEM as a Cloud Service을 준비하려면 [저장소 구조 변경](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) 을 참조하십시오.
* 저장소의 변경 가능 및 변경할 수 없는 영역에 대한 자세한 내용은 [AEM 프로젝트 구조](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) 를 참조하십시오.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
* [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools)를 활용하여 콘텐츠와 코드를 개별 패키지로 분리하여 Adobe Experience Manager에 대해 정의된 Cloud Service 구조와 호환되도록 함으로써 기존 프로젝트 패키지를 재구성합니다.
