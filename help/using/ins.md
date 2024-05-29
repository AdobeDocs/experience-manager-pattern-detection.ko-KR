---
title: INS
description: 패턴 감지기 코드 도움말 페이지.
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: ht
source-wordcount: '109'
ht-degree: 100%

---

# INS {#ins}

잘못된 네임스페이스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="잘못된 네임스페이스"
>abstract="INS는 AEM 인스턴스에서의 네임스페이스 문제를 식별합니다."

`INS`(잘못된 네임스페이스)는 AEM 인스턴스에서의 네임스페이스 문제를 식별합니다.

다양한 유형의 정보 식별을 위해 다음과 같은 하위 유형이 사용됩니다.

* `uri`: AEM에서 잘못된 네임스페이스 URI를 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 콘텐츠를 복제(계층 간)하거나 콘텐츠를 복사(`/crx/packMgr` 또는 콘텐츠 복사를 통해 `env` 간)할 수 없습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="구현 지침"
>abstract="도움이 필요한 경우 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* [JCR 사양](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html)에 따라 네임스페이스 정의를 수정하십시오. [여기](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)에 기재되어 있는 단계를 따르십시오.
* 자세한 설명이 필요하거나 문제를 해결하려면 [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
