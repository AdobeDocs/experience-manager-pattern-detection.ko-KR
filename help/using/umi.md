---
title: UMI
description: 패턴 감지기 코드 도움말 페이지..
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 40%

---

# UMI {#umi}

업그레이드 구성 오류 문제

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="업그레이드 구성 오류 문제"
>abstract="UMI는 업그레이드 실패 또는 기능 축소와 같이 업그레이드 시 문제를 발생시키는 특정 OSGi 구성에 대한 변경 내용을 식별합니다."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="주요 변경 내용 - AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - 릴리스 정보"

UMI는 업그레이드 실패 또는 기능 축소와 같이 업그레이드 시 문제를 발생시키는 특정 OSGi 구성에 대한 변경 내용을 식별합니다.

다음 구성이 수정된 것으로 확인되었습니다.

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config`: 사용자 정의 로거의 `org.apache.sling.commons.log.file` 속성이 `logs/error.log` 파일 이외의 항목을 가리키는지 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* 구성을 변경 또는 제거하면 다음과 같은 문제가 발생할 수 있습니다.
   * 업그레이드가 멈출 수 있습니다(예: `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`이 누락되었지만 `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`에 존재함).
   * 업그레이드 이후 인증 문제가 발생할 수 있습니다(`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * 특정 기능이 예상대로 작동하지 않을 수 있습니다. 예: 변경 `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` 일부 JSP 파일이 컴파일되지 않아 궁극적으로 기능 손실이 발생할 수 있습니다.
   * Externalizer 구성의 값 `com.day.cq.commons.impl.ExternalizerImpl` 는 AEM as a Cloud Service으로 cloud manager 환경 변수에 의해 설정됩니다.
   * AEM as a Cloud Service가 사용자 정의 로그 파일을 지원하지 않습니다. 사용자 지정 로그에 기록된 로그를 AEM에서 as a Cloud Service으로 액세스할 수 없습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="구현 지침"
>abstract="가장 좋은 방법은 현재 구성을 검토하고 언급된 구성에 대한 변경 내용을 되돌려 향후 발생할 업그레이드 문제를 방지하는 것입니다. 도움 또는 설명이 필요한 경우 Adobe 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 위에서 언급한 4가지의 구성을 변경하거나 제거하지 마십시오.
   * 다음 위반이 있는 경우:\
     &quot;OSGi 구성에 필요한 속성 `xyz-configuration` 누락됨: &#39;[속성-1, 속성-2...]&#39;.&#39;\
     이러한 OSGI 구성이 OOTB이며 OSGi 구성 관리자에서 수정/저장된 적이 없을 수 있으므로 이러한 삭제가 적법한지 여부를 확인합니다.
* 구성을 변경한 경우 예상 값으로 다시 복원해야 합니다. 이들 값은 `UMI` 메시지에 기재되어 있습니다.
* 대상 `com.day.cq.commons.impl.ExternalizerImpl`, 참조 [설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) AEMas a Cloud Service 에서 클라우드 관리자 환경 변수를 사용하여 외부화 구성 설정.
* `org.apache.sling.commons.log.LogManager.factory.config`의 경우 OSGI 구성을 사용자 정의된 로거가 `logs/error.log` 파일로 전송될 수 있도록 변경하십시오. 다음을 참조하십시오 [설명서](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) 을(를) 다시 가리키기 위해 `logs/error.log` 파일.
* 다음으로 문의: [AEM 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명이 필요하거나 문제가 해결되었습니다.
