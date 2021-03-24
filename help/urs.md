---
title: 흐림 효과
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# {#urs}

지원되지 않는 저장소 구조

## 배경 {#background}

`URS` 지원되지 않는 저장소 구조의 경우를 식별합니다. AEM 6.4부터 저장소 컨텐츠의 재구성에 대한 지침이 제공됩니다. AEM 제품 코드와 고객 코드에 대한 계층을 명확히 정의하고 이러한 계층 간 충돌을 방지함으로써 컨텐츠가 `/etc`에서 저장소의 다른 폴더로 재구성되었으며 다음과 같은 고급 규칙을 따릅니다.

* AEM 제품 코드는 항상 `/libs`에 삽입되며, 이 코드는 사용자 지정 코드로 덮어쓰지 않아야 합니다. 사용자 지정 코드는 `/apps`, `/content` 및 `/conf`에 삽입해야 합니다.
* 이 지침들은 Cloud Service의 경우 AEM에 따라 수행하는 것이 좋습니다.

하위 유형은 해결해야 하는 특정 유형의 저장소 문제를 식별하는 데 사용됩니다.
* `clientlibs.location`:경로 `/etc` 로 참조하는 클라이언트 라이브러리
* `file.location`:설치 후 `/etc` 에 수정된 파일.
* `node.location`:설치 후 `/etc` 에 수정된 노드 아래에 있습니다.
* `workflow.location`:아래의 워크플로우 모델 또는 런처 `/etc/workflow`.
* `package.structure`:변경할 수 없는 컨텐츠와 변경할 수 없는 컨텐츠를 모두 포함하는 패키지입니다.

## 가능한 의미 및 위험 {#implications-and-risks}

* 이전 경로에 의존하는 사용자 지정 코드는 원치 않는 비헤이비어를 유발하고 제품 기능에 영향을 줄 수 있습니다.
* 변경할 수 없는 컨텐츠와 변경할 수 없는 컨텐츠를 모두 포함하는 패키지는 배포 중에 문제를 일으킬 수 있습니다.

## 가능한 솔루션 {#solutions}

* AEM을 Cloud Service으로 준비하는 방법에 대한 지침은 [저장소 재구성](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html)을 참조하십시오.
* 저장소의 변경 및 변경 불가능한 영역에 대한 자세한 내용은 [AEM 프로젝트 구조](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html)를 참조하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
* [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools)를 활용하면 Adobe Experience Manager에 대해 Cloud Service으로 정의된 프로젝트 구조와 호환되도록 컨텐츠와 코드를 개별 패키지로 구분하여 기존 프로젝트 패키지를 재구성할 수 있습니다.