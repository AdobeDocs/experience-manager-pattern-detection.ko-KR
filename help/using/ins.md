---
title: INS
description: 패턴 감지기 코드 도움말 페이지
source-git-commit: e469b546a75a77e538a54de3ffc1ca385c8cf21d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 47%

---

# INS {#ins}

잘못된 네임스페이스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="잘못된 네임스페이스"
>abstract="INS는 AEM 인스턴스에서 네임스페이스 문제를 식별합니다"

`INS`  잘못된 네임스페이스는 AEM 인스턴스에서 네임스페이스 문제를 식별합니다.

다양한 유형의 정보 식별을 위해 다음과 같은 하위 유형이 사용됩니다.

* `uri`: AEM에서 잘못된 네임스페이스 URI를 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 계층 간에 콘텐츠를 복제하거나 환경 간에 콘텐츠를 복사할 수 없음 `/crx/packMgr` 또는 콘텐츠 사본)을 참조하십시오.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="구현 지침"
>abstract="도움이 필요한 경우 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 다음에 따라 네임스페이스 정의를 수정합니다. [JCR 사양](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). 언급된 단계 수행 [여기](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)
* 자세한 설명이 필요하거나 문제를 해결하려면 [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.