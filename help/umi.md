---
title: UMI
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# UMI {#umi}

업그레이드 구성 오류 문제

## 배경 {#background}

`UMI` 업그레이드 실패 또는 감소 기능을 포함하여 업그레이드 시 문제를 야기할 특정 OSGi 구성의 수정 사항을 확인합니다.

다음 구성을 수정하여 수정합니다.
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## 가능한 의미 및 위험 {#implications-and-risks}

* 구성을 변경하거나 제거하면 다음과 같은 문제가 발생할 수 있습니다.
   * 업그레이드가 중단될 수 있습니다(예: `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`이(가) 누락되었지만 `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`에 있음).
   * 인증 문제는 업그레이드(`org.apache.sling.engine.impl.auth.SlingAuthenticator`) 후에 발생할 수 있습니다.
   * 특정 기능은 예상대로 작동하지 않을 수 있습니다. 예를 들어 `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`을 변경하면 일부 JSP 파일이 컴파일되지 않을 수 있으므로 결과적으로 기능이 손실될 수 있습니다.

## 가능한 솔루션 {#solutions}

* 위에 언급된 4개의 구성을 변경하거나 제거하지 마십시오.
* 구성이 변경된 경우 해당 구성을 예상 값으로 복원해야 합니다. 이러한 값은 `UMI` 메시지에 표시됩니다.
* 명확히 파악하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
