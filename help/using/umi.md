---
title: UMI
description: 패턴 감지기 코드 도움말 페이지.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 87%

---

# UMI {#umi}

업그레이드 구성 오류 문제

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="업그레이드 구성 오류 문제"
>abstract="UMI는 업그레이드 실패 또는 기능 축소와 같이 업그레이드 시 문제를 발생시키는 특정 OSGi 구성에 대한 변경 내용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - 릴리스 정보"

`UMI`는 업그레이드 실패 또는 기능 축소와 같이 업그레이드 시 문제를 발생시키는 특정 OSGi 구성에 대한 변경 내용을 식별합니다.

다음 구성이 수정된 것으로 확인되었습니다.

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config` : 다음 여부를 식별합니다. `org.apache.sling.commons.log.file` 사용자 지정 로거의 속성이 `logs/error.log` 파일.

## 가능한 영향 및 위험 {#implications-and-risks}

* 구성을 변경하거나 제거하면 다음 문제가 발생할 수 있습니다.
   * 업그레이드가 멈출 수 있습니다(예: `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`이 누락되었지만 `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`에 존재함).
   * 업그레이드 이후 인증 문제가 발생할 수 있습니다(`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * 특정 기능이 예상대로 작동하지 않을 수 있습니다. 예를 들어 `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`를 변경하면 일부 JSP 파일이 컴파일되지 않아 궁극적으로 기능 손실이 발생할 수 있습니다.
   * Externalizer 구성의 값 `com.day.cq.commons.impl.ExternalizerImpl` AEM as a Cloud Service으로 cloud manager 환경 변수를 사용하여 설정됩니다.
   * AEM as a Cloud Service가 사용자 정의 로그 파일을 지원하지 않습니다. 사용자 정의 로그에 기록된 로그를 AEM as a Cloud Service에서 액세스할 수 없습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 현재 구성을 검토하고 언급된 구성에 대한 변경 내용을 이전으로 되돌려 향후 발생할 업그레이드 문제를 방지하는 것입니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 위에서 언급한 4가지의 구성을 변경하거나 제거하지 마십시오.
   * 다음과 같은 위반 사항이 있는 경우:\
     “OSGi 구성 `xyz-configuration`에 대한 필수 속성 누락: “[property-1, property-2 ...]”.”\
     이러한 OSGI 구성이 OOTB이며 OSGi 구성 관리자에서 수정되거나 저장된 적이 없을 수 있으므로 이러한 삭제가 적절한지 확인하십시오.
* 구성을 변경한 경우 예상 값으로 다시 복원해야 합니다. 이들 값은 `UMI` 메시지에 기재되어 있습니다.
* `com.day.cq.commons.impl.ExternalizerImpl`에 대해서는 AEM as a Cloud Service의 클라우드 관리자 환경 변수를 사용하여 외부화 구성 설정하기에 대한 [설명서](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer)를 참조하십시오.
* `org.apache.sling.commons.log.LogManager.factory.config`의 경우 OSGI 구성을 사용자 정의된 로거가 `logs/error.log` 파일로 전송될 수 있도록 변경하십시오. [설명서](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs)를 통해 `logs/error.log` 파일을 다시 가리키도록 하는 방법을 살펴보십시오.
* 자세한 내용을 확인하거나 문제를 해결하려면 [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
