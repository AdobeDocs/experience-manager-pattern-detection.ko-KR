---
title: 유미
description: 패턴 탐지기 코드 도움말 페이지
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 3%

---

# 유미 {#umi}

잘못된 구성 업그레이드 문제

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="잘못된 구성 업그레이드 문제"
>abstract="UMI는 업그레이드 실패 또는 기능 감소 등 업그레이드 시 문제를 일으키는 특정 OSGi 구성의 수정 사항을 식별합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="주요 변경 사항 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=ko-KR" text="AEM as a Cloud Service - 릴리스 노트"

`UMI` 는 업그레이드 실패 또는 기능 감소 등 업그레이드 시 문제를 일으킬 특정 OSGi 구성의 수정 사항을 확인합니다.

다음 구성에 수정 사항이 있는지 확인합니다.
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## 가능한 의미 및 위험 {#implications-and-risks}

* 구성을 변경하거나 제거하면 다음과 같은 문제가 발생할 수 있습니다.
   * 업그레이드가 중단될 수 있습니다(예: `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` 이 누락되었지만 `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`에 있음).
   * 업그레이드 후 인증 문제가 발생할 수 있습니다(`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * 특정 기능이 예상대로 작동하지 않을 수 있습니다. 예를 들어 `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` 을 변경하면 일부 JSP 파일이 컴파일되지 않을 수 있으므로 결과적으로 기능이 손실될 수 있습니다.

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 현재 구성을 검토하고 언급된 구성에 대한 변경 사항을 되돌려서 향후 업그레이드 문제를 방지하는 것입니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 위에 언급된 4개의 구성을 변경하거나 제거하지 마십시오.
* 구성이 변경된 경우 예상한 값으로 복원해야 합니다. 이러한 값은 `UMI` 메시지에 표시됩니다.
* 명확히 하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
