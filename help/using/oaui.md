---
title: OAUI
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: ht
source-wordcount: '228'
ht-degree: 100%

---

# OAUI {#oaui}

OAuth 사용자 인스턴스

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="OAuth 사용자 인스턴스"
>abstract="OAUI 코드는 최소 한 명 이상의 올바른 마이그레이션이 필요한 OAuth 관련 구성된 사용자가 있는 패턴을 식별합니다. `rep:AuthorizableId` 노드의 바로 아래에 `oauth`라는 이름의 하위 노드가 `/home/user-path/user-node/oauth`의 형식으로 존재하는 경우 사용자에 대해 OAuth가 구성됩니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - 릴리스 정보"

`OAUI`는 최소 한 명 이상의 올바른 마이그레이션이 필요한 OAuth 관련 구성된 사용자가 있는 패턴을 식별합니다.

`rep:AuthorizableId` 노드의 바로 아래에 `oauth`라는 이름의 하위 노드가 `/home/user-path/user-node/oauth`의 형식으로 존재하는 경우 사용자에 대해 OAuth가 구성됩니다.

예: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`

## 가능한 영향 및 위험 {#implications-and-risks}

* OAuth로 구성된 외부 사용자는 아래 절차를 통해 재구성할 때까지 작성자/게시 인스턴스에 로그인할 수 없습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="구현 지침"
>abstract="OAuth로 구성된 외부 사용자는 AEM as a Cloud Service와 호환되도록 재구성되기 전까지 작성자/게시 인스턴스에 로그인할 수 없습니다. AEM as a Cloud Service에서는 작성자, 관리자 및 개발자 사용자에 대해서만 IMS 인증 지원 서비스를 제공하며 게시 환경에 대한 SAML 기반 통합 기능을 제공합니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/security/ims-support" text="IMS 지원 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="SAML 통합 - 게시"

* 사용자 마이그레이션 옵션에 대해 논의가 필요한 경우 Adobe 담당자에게 문의하십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
