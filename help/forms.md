---
title: Forms.
description: 패턴 탐지기 코드 도움말 페이지
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## 배경 {#background}

`FORMS` Adobe Experience Manager Forms에서 Adobe Experience Manager Forms으로 마이그레이션하는 것과 관련된 잠재적 문제를 Cloud Service으로 식별합니다. Cloud Service으로 마이그레이션하기 전에 이러한 문제를 해결합니다.

다음 하위 유형은 서로 다른 유형의 문제를 식별하는 데 도움이 됩니다.

* `modified.feature`:이러한 기능, 자산 또는 API는 Cloud Service에 대해 업데이트되거나 수정되었습니다. Cloud Service으로 마이그레이션하기 전에 마이그레이션 유틸리티를 실행하여 이러한 기능과 에셋이 Cloud Service과 호환되도록 합니다.
* `unavailable.feature`:사용 가능한 기능 및 에셋이 없거나 Cloud Service에서 제거됩니다. 이러한 기능 또는 자산을 Cloud Service 환경으로 마이그레이션하지 마십시오.
* `unsupported.feature`:Cloud Service에서 지원되지 않는 일부 기능이 사용 중입니다. 이러한 기능 또는 자산을 Cloud Service 환경으로 마이그레이션하지 마십시오. 기능을 사용할 수 있는지 매월 릴리스 노트를 확인해 보십시오.
* `unsupported.api`:환경에 일부 API가 아직 Cloud Service에서 지원되지 않습니다. Cloud Service으로 마이그레이션하기 전에 코드에서 이러한 API를 비활성화, 교체 또는 제거합니다. 기능을 사용할 수 있는지 매월 릴리스 노트를 확인해 보십시오.

Cloud Service과 호환되는 일부 기능 및 API를 만드는 데 필요한 교체 및 기타 작업에 대한 자세한 내용은 [가능한 함수와 위험](#implications-and-risks) 및 [가능한 솔루션](#solutions) 섹션을 참조하십시오

## 가능한 의미 및 위험 {#implications-and-risks}

Cloud Service으로 Adobe Experience Manager Forms으로 마이그레이션하기 전에 다음 문제를 해결하십시오. 아래에 열거된 의미 및 위험 요소를 해결하지 않으면 일부 기능이 Cloud Service 환경에서 예상대로 작동하지 않습니다.

* 규칙 편집기 기능의 코드 편집기 기능을 사용할 수 없습니다. (CODE_EDITOR)

* 이메일 지원(SMTP 포트)은 기본적으로 비활성화되어 있습니다. (EMAIL_SERVICE_CONFIGURATION)

* **[!UICONTROL PDF]** 제출 작업을 사용할 수 없습니다.(EMAIL_PDF_SUBMIT_ACTION)

* XDP 기반의 적응형 양식은 아직 지원되지 않습니다. (XDP_BASED_FORM)

* 모든 서명자가 서명을 완료할 때까지 기다리지 않고 양식 제출 작업을 즉시 호출할 수 있습니다. 따라서 사용 또는 처리할 제출 작업에 적응형 양식 서명 문서(서명자에게 보낸 Adobe Sign 계약 PDF)를 사용할 수 없습니다. (FORM_SIGN_INTEGRATION)

* 서명 단계를 사용할 수 없습니다. (SIGNATURE_STEP)

* 확인 단계를 사용할 수 없습니다. (VERIFY_STEP)

* Forms Portal 기능 및 **[!UICONTROL Forms Portal 제출 작업]**&#x200B;을 사용할 수 없습니다. Forms Portal을 사용하여 양식을 나열하거나 초안을 저장하거나 제출된 양식을 표시할 수 없습니다. 적응형 양식에 제출된 데이터를 Forms Portal에 전송(**[!UICONTROL Forms Portal 제출 작업]** 사용)할 수 없습니다. [!UICONTROL 현재] 는 자동 저장  [!UICONTROL 적응형 ] 양식 기능이 지원되지 않습니다. (FORMS._PORTAL_SUBMISSION, FORMS._PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* **[!UICONTROL Forms 작업 과정에 제출]** 제출 작업을 사용할 수 없습니다. AEM 6.5 Forms 및 이전 버전에서 제출 작업은 JEE 워크플로우 및 LiveCycle Workflow의 기존 AEM Forms에 적응형 양식 데이터를 제출하는 데 사용되었습니다. (LC_WORKFLOW_SUBMISSION)

* 대화형 통신 기능을 사용할 수 없습니다.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL 현재]** 는 자동 저장  **[!UICONTROL 적응형]** 양식 기능이 지원되지 않습니다. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* 메타데이터 아코디언을 사용할 수 없습니다. (METADATA_ACCORDION_FORM_CONTAINER)

* 이제 CAPTCHA 구성 요소는 Google reCAPTCHA 서비스를 사용하여 기본적으로 CAPTCHA의 유효성을 확인합니다. Adobe Experience Manager을 사용하여 CAPTCHA의 유효성을 검사하는 옵션은 사용할 수 없습니다. (FORMS._CAPTCHA)

## 가능한 솔루션 {#solutions}

* 마이그레이션 유틸리티를 사용하여 환경에 있는 모든 규칙 스크립트를 재사용 가능한 함수로 변환할 수 있습니다. 시각적 규칙 편집기에서 재사용 가능한 함수를 사용하여 규칙 스크립트로 얻은 결과를 계속 얻을 수 있습니다. (CODE_EDITOR)

* 환경에 대한 이메일(SMTP 포트 열기) 기능을 활성화하려면 지원 팀에 문의하십시오. 기본적으로 나가는 HTTP 및 HTTPS 연결만 활성화됩니다. (EMAIL_SERVICE_CONFIGURATION)

* **[!UICONTROL 전자 메일 PDF]** 대신 **[!UICONTROL 전자 메일]** 제출 작업을 사용합니다. **[!UICONTROL 이메일]** 제출 작업에서는 첨부 파일을 보내고 문서(DoR)를 전자 메일에 첨부하는 옵션을 제공합니다. (EMAIL_PDF_SUBMIT_ACTION)

* XDP 기반 적응형 양식을 Cloud Service 환경으로 마이그레이션하지 마십시오. 기능을 사용할 수 있는지 매월 릴리스 노트를 확인해 보십시오. (XDP_BASED_FORM)

* 제출된 데이터에 서명 계약 ID가 포함됩니다. 필요한 경우 서명 계약 ID를 사용하여 서명 계약 PDF를 검색할 수 있습니다.  (FORM_SIGN_INTEGRATION)

* 적응형 양식의 서명 단계를 동일한 창에서 적응형 양식 게시물 제출 문서에 서명하는 옵션으로 바꿉니다. 브라우저 내 서명 경험](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684)을 계속 제공하는 데 도움이 됩니다. [ (SIGNATURE_STEP)

* 기존 적응형 양식에서 확인 단계를 제거한 다음 해당 양식을 Cloud Service 환경으로 이동합니다. (VERIFY_STEP)

* **[!UICONTROL Forms 포털 제출 작업]**&#x200B;에 대한 대안이 없습니다. Cloud Service에 대해 Forms Portal 기능이 릴리스되면 이 제출 작업을 사용할 수 있습니다. 기능을 사용할 수 있는지 매월 릴리스 노트를 확인해 보십시오. (FORMS._PORTAL_SUBMISSION, FORMS._PORTAL)

* **[!UICONTROL Forms 작업 과정에 제출]** 작업 제출 시 다른 제출 작업이 없습니다. 사용자 정의 제출 작업을 개발하여 데이터, 첨부 파일 또는 기록 문서(DoR)를 LiveCycle 프로세스로 전송할 수 있습니다. (LC_WORKFLOW_SUBMISSION)

* 인터랙티브 커뮤니케이션, 문자 및 관련 사전을 Cloud Service 환경으로 마이그레이션하지 마십시오. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Cloud Service으로 마이그레이션하기 전에 적응형 양식에서 **[!UICONTROL 초안]** 및 **[!UICONTROL 자동 저장 사용]** 옵션을 비활성화하십시오. Cloud Service에 대해 Forms Portal 기능이 릴리스되면 이러한 옵션을 활성화할 수 있습니다. 기능을 사용할 수 있는지 매월 릴리스 노트를 확인해 보십시오. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* 메타데이터 아코디언을 대체할 수 없습니다. 양식에서 Cloud Service으로 마이그레이션하기 전에 양식을 제거합니다.(METADATA_ACCORDION_FORM_CONTAINER)

* Adobe Experience Manager에서 제공하는 CAPTCHA 서비스 대신 Google reCaptcha를 사용하십시오. (FORMS._CAPTCHA)

명확히 파악하거나 문제를 해결하려면 [Adobe 지원](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
