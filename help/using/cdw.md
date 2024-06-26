---
title: CDW
description: 패턴 감지기 코드 도움말 페이지.
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: d1c652a8a45a081661ffe4443f85fcc932947541
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 100%

---

# CDW {#cdw}

사용자 정의 대화 상자 위젯

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="사용자 정의 대화 상자 위젯"
>abstract="CDW는 AEM as a Cloud Service와 호환되도록 업데이트해야 하는 사용자 정의 대화 상자 위젯을 식별합니다."

`CDW`  (`Custom Dialog Widgets`) 사용자 정의 클래식 대화 상자 위젯을 식별합니다. AEM as a Cloud Service와 호환되도록 이들 위젯을 업데이트해야 합니다.

정보 식별을 위해 다음과 같은 하위 유형이 사용됩니다.

* `custom.classic.widget`: ExtJs를 기반으로 사용자 정의 대화 상자 위젯을 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 클래식 UI는 AEM as a Cloud Service에서 더 이상 사용할 수 없습니다. 제작을 위한 표준 인터페이스는 터치 기능이 지원되는 UI입니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="구현 지침"
>abstract="도움이 필요한 경우 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 사용자 정의 클래식 대화 상자 위젯은 ExtJS에서 [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html)로 변환되어야 합니다.
* 자세한 설명이 필요하거나 문제를 해결하려면 [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
