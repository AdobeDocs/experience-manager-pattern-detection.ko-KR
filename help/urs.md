---
title: URS
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 3e14d73acbe480dd861f492c24f67ffc37b1090d
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 3%

---

# URS {#urs}

지원되지 않는 저장소 구조

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="지원되지 않는 저장소 구조"
>abstract="URS는 지원되지 않는 저장소 구조 및 노드 특성의 사례를 식별합니다. 이는 AEM 제품 코드와 고객 코드 간의 충돌, /etc에서 저장소의 다른 폴더로 재구성된 컨텐츠 등을 방지하기 위한 정보를 나타냅니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="저장소 구조 변경"

## 배경 {#background}

`URS` 지원되지 않는 저장소 구조 및 노드 특성의 사례를 식별합니다. AEM 6.4부터 저장소 컨텐츠 재구성에 대한 지침이 제공되었습니다. AEM 제품 코드와 고객 코드에 대한 계층을 명확하게 설명하고 두 코드 간의 충돌을 방지하여 컨텐츠가 재구성되었습니다 `/etc` 저장소의 다른 폴더에 대해 다음 고급 규칙을 준수합니다.

* AEM 제품 코드는 항상 `/libs`: 사용자 지정 코드로 덮어쓰지 않아야 합니다.
* 사용자 지정 코드는 `/apps`, `/content` 및 `/conf`.
* AEM as a Cloud Service은 긴 노드 이름(>150바이트)을 지원하지 않습니다.
* AEM as a Cloud Service에 대해 이러한 지침을 따르는 것이 좋습니다.

하위 유형은 해결해야 하는 특정 유형의 저장소 문제를 식별하는 데 사용됩니다.
* `clientlibs.location`: 참조하는 클라이언트 라이브러리 `/etc` 경로 기준.
* `file.location`: 아래의 파일 `/etc` 이 수정 사항은 설치 후 수정되었습니다.
* `node.location`: 아래의 노드 `/etc` 이 수정 사항은 설치 후 수정되었습니다.
* `workflow.location`: 아래의 워크플로우 모델 또는 런처 `/etc/workflow`.
* `package.structure`: 변경할 수 있는 컨텐츠와 변경할 수 없는 컨텐츠를 모두 포함하는 패키지입니다.
* `node.name.length`: 지원되지 않는 길이의 노드 이름입니다.
* `node.size`: 지원되지 않는 크기의 노드입니다.

## 가능한 의미와 위험 {#implications-and-risks}

* 이전 경로에 의존하는 사용자 지정 코드는 원치 않는 동작과 제품 기능에 영향을 줄 수 있습니다.
* 변경할 수 있는 컨텐츠와 변경할 수 없는 컨텐츠를 모두 포함하는 패키지는 배포 중에 문제를 일으킬 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 코드 프로젝트를 검토하고 AEM 프로젝트 구조 지침을 준수하고 AEM as a Cloud Service에서 원치 않는 동작을 초래할 수 있는 오래된/지원되지 않는 저장소 경로에 코드를 의존하는 것을 방지하는 것입니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="AEM 프로젝트 구조 지침"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 을(를) 참조하십시오. [저장소 구조 변경](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) AEM as a Cloud Service에 대한 지침을 제공합니다.
* 또한 [AEM 프로젝트 구조](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) 저장소의 변경할 수 있고 변경할 수 없는 영역에 대해 자세히 알아보십시오.
* 연락하여 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) 명확히 하거나 문제를 해결하기 위해.
* 활용 [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) Adobe Experience Manager as a Cloud Service에 대해 정의된 프로젝트 구조와 호환되도록 컨텐츠 및 코드를 개별 패키지로 분리하여 기존 프로젝트 패키지를 재구성하는 방법
