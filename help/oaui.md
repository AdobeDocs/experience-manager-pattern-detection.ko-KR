---
title: OAUI
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 3%

---

# OAUI {#oaui}

OAuth 사용자 인스턴스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth 사용자 인스턴스"
>abstract="OAUI 코드는 올바른 마이그레이션이 필요한 하나 이상의 OAuth 관련 구성 사용자가 있는 패턴을 식별합니다. oauth라는 하위 노드가 /home/user-path/user-node/oauth 형식의 rep:AuthorizableId 노드 바로 아래에 있을 때 OAuth가 사용자에 대해 구성됩니다"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR" text="AEM을 Cloud Service - 릴리스 노트"

`OAUI` 올바른 마이그레이션이 필요한 하나 이상의 OAuth 관련 구성 사용자가 있는 패턴을 식별합니다.

`/home/user-path/user-node/oauth` 형식의 `rep:AuthorizableId` 노드 바로 아래에 `oauth`이라는 하위 노드가 있는 경우 OAuth는 사용자를 위해 구성됩니다.

예:`/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## 가능한 의미 및 위험 {#implications-and-risks}

* OAuth로 구성된 외부 사용자는 아래 절차에 따라 다시 구성할 때까지 작성자/게시 인스턴스에 로그인할 수 없습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="구현 지침"
>abstract="OAuth로 구성된 외부 사용자는 AEM과 Cloud Service을 호환하도록 재구성되기 전까지는 작성자/게시 인스턴스에 로그인할 수 없습니다. AEM은 Cloud Service의 경우 게시 환경에 대한 작성자, 관리자 및 개발자 사용자에 대해서만 IMS 인증 지원을 제공하고 SAML 기반 통합을 제공합니다. 도움말 및 분류에 대한 Adobe 지원"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html" text="IMS 지원 - Cloud Service의 AEM"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=en#integration-with-an-idp" text="SAML 통합 - 게시"

* 사용자 마이그레이션 옵션에 대해 논의하려면 Adobe 담당자에게 문의하십시오.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
