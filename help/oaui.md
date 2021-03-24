---
title: OAUI
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# OAUI {#oaui}

OAuth 사용자 인스턴스

## 배경 {#background}

`OAUI` 올바른 마이그레이션이 필요한 하나 이상의 OAuth 관련 구성 사용자가 있는 패턴을 식별합니다.

`/home/user-path/user-node/oauth` 형식의 `rep:AuthorizableId` 노드 바로 아래에 `oauth`이라는 하위 노드가 있는 경우 OAuth는 사용자를 위해 구성됩니다.

예:`/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## 가능한 의미 및 위험 {#implications-and-risks}

* OAuth로 구성된 외부 사용자는 아래 절차에 따라 다시 구성할 때까지 작성자/게시 인스턴스에 로그인할 수 없습니다.

## 가능한 솔루션 {#solutions}

* 사용자 마이그레이션 옵션에 대해 논의하려면 Adobe 담당자에게 문의하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
