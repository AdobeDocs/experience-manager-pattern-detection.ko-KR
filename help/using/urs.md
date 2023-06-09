---
title: URS
description: 패턴 감지기 코드 도움말 페이지
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '436'
ht-degree: 100%

---

# URS {#urs}

지원되지 않는 저장소 구조

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="지원되지 않는 저장소 구조"
>abstract="URS는 지원되지 않는 저장소 구조 및 노드 특성에 대한 사례를 식별합니다. 여기에는 AEM 제품 코드와 고객 코드 간의 충돌을 방지하기 위한 정보, /etc에서 저장소의 다른 폴더로 재구성되는 콘텐츠 등이 표시됩니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="저장소 재구성"

## 배경 {#background}

`URS`는 지원되지 않는 저장소 구조 및 노드 특성에 대한 사례를 식별합니다. AEM 6.4부터 저장소 콘텐츠 재구성을 위한 지침이 제공되고 있습니다. AEM 제품 코드 및 고객 코드에 대한 계층을 명확하게 기술하고 상호 간의 충돌을 방지함으로써, 콘텐츠는 다음과 같은 높은 수준의 규칙을 준수하며 `/etc`에서 저장소의 다른 폴더로 재구성되고 있습니다.

* AEM 제품 코드는 항상 `/libs`에 배치되며, 이는 사용자 지정 코드로 덮어쓸 수 없습니다.
* 사용자 지정 코드는 `/apps`, `/content` 및 `/conf`에 배치해야 합니다.
* AEM as a Cloud Service는 150바이트를 초과하는 긴 노드 이름을 지원하지 않습니다.
* AEM as a Cloud Service에 대해 이들 지침을 따르는 것이 좋습니다.

해결이 필요한 특정 유형의 저장소 문제를 식별하기 위해 다음과 같은 하위 유형이 사용됩니다.
* `clientlibs.location`: 패스를 통해 `/etc`를 참조하는 클라이언트 라이브러리
* `file.location`: 설치 이후 수정된 `/etc` 하의 파일
* `node.location`: 설치 이후 수정된 `/etc` 하의 노드
* `workflow.location`: `/etc/workflow` 하의 워크플로 모델 또는 런처
* `package.structure`: 변경 가능한 콘텐츠 및 변경 불가능한 콘텐츠가 모두 포함된 패키지
* `node.name.length`: 지원되지 않는 길이의 노드 이름
* `node.size`: 지원되지 않는 크기의 노드

## 가능한 영향 및 위험 {#implications-and-risks}

* 이전 패스에 의존하는 사용자 지정 코드를 사용하면 원하지 않는 비헤이비어가 발생할 수 있으며 제품 기능에 영향을 줄 수 있습니다.
* 변경 가능한 콘텐츠 및 변경 불가능한 콘텐츠가 모두 포함된 패키지를 사용하면 배포 도중 문제가 발생할 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 코드 프로젝트를 검토하여 AEM 프로젝트 구조 지침을 준수하도록 하고 이전/지원되지 않는 저장소 패스에 의존하여 AEM as a Cloud Service에서 원하지 않은 비헤이비어를 야기할 수 있는 코드를 사용하지 않는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="AEM 프로젝트 구조 지침"
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* AEM as a Cloud Service를 준비하기 위한 지침을 얻으려면 [저장소 재구성](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html)을 참조하십시오.
* 또한 [AEM 프로젝트 구조](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html)를 참조하여 변경 가능한/변경 불가능한 저장소 영역에 대해 자세히 알아보십시오.
* 자세한 설명이 필요하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
* [저장소 현대화 도구](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools)를 통해 콘텐츠 및 코드를 Adobe Experience Manager as a Cloud Service에 대해 정의된 프로젝트 구조와 호환될 수 있도록 개별 패키지로 분리하여 기존 프로젝트 패키지를 재구성하십시오.
