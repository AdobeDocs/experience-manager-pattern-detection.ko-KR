---
title: 양식
description: 패턴 탐지기 코드 도움말 페이지
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '1228'
ht-degree: 0%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="Forms."
>abstract="Forms. 코드는 Adobe Experience Manager Forms에서 Adobe Experience Manager Forms으로 마이그레이션하는 것과 관련된 잠재적 문제를 Cloud Service으로 식별합니다. Cloud Service으로 마이그레이션하기 전에 관련 가능한 암시적 및 위험을 검토하고 이러한 문제를 해결합니다."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-pattern-detection/table-of-contents/forms.html#implications-and-risks" text="가능한 의미와 위험"

`FORMS` 에서 로 마이그레이션과 관련된 잠재적 문제 [!DNL Adobe Experience Manager Forms] 를  [!DNL Adobe Experience Manager Form]로  [!DNL Cloud Service]식별합니다. [!DNL Cloud Service](으)로 마이그레이션하기 전에 이러한 문제를 해결합니다.

다음 하위 유형은 다양한 유형의 문제를 식별하는 데 도움이 됩니다.

* `modified.feature`:이러한 기능, 자산 또는 API는 Cloud Service을 위해 업데이트되거나 수정되었습니다. Cloud Service으로 마이그레이션하기 전에 마이그레이션 유틸리티를 실행하여 이러한 기능과 Cloud Service과 호환되는 자산을 만듭니다.
* `unavailable.feature`:환경에 사용할 수 없거나 Cloud Service에서 제거된 기능과 자산이 있습니다. 이러한 기능 또는 자산을 Cloud Service 환경으로 마이그레이션하지 마십시오.
* `unsupported.feature`:환경에서 Cloud Service에서 지원되지 않는 일부 기능을 사용하고 있습니다. 이러한 기능 또는 자산을 Cloud Service 환경으로 마이그레이션하지 마십시오. 기능 가용성에 대한 자세한 내용은 월별 릴리스 노트를 참조하십시오.
* `unsupported.api`:Cloud Service에서 아직 지원되지 않는 API가 환경에 있습니다. Cloud Service으로 마이그레이션하기 전에 코드에서 이러한 API를 비활성화, 바꾸기 또는 제거합니다. 기능 가용성에 대한 자세한 내용은 월별 릴리스 노트를 참조하십시오.

Cloud Service과 호환되는 일부 기능 및 API를 만드는 데 필요한 대체 및 기타 작업에 대한 정보는 [가능한 의미와 위험](#implications-and-risks) 및 [가능한 솔루션](#solutions) 섹션을 참조하십시오

## 가능한 의미 및 위험 {#implications-and-risks}

[!DNL Adobe Experience Manager Forms as a Cloud Service](으)로 마이그레이션하기 전에 다음 문제를 해결하십시오. 아래에 나열된 의미 및 위험을 해결하지 않으면 일부 기능이 Cloud Service 환경에서 예상대로 작동하지 않습니다.

* 규칙 편집기 기능의 코드 편집기 기능을 사용할 수 없습니다. (CODE_EDITOR)

* 전자 메일 지원(SMTP 포트)은 기본적으로 비활성화됩니다. (EMAIL_SERVICE_CONFIGURATION)

* **[!UICONTROL 전자 메일 PDF]** 제출 작업을 사용할 수 없습니다.(EMAIL_PDF_SUBMIT_ACTION)

* XFA 기반 응용 Forms은 아직 지원되지 않습니다. (XFA_BASED_FORM, XDP_BASED_FORM)

* 모든 서명자가 서명을 완료할 때까지 기다리는 대신 양식 제출 시 제출 작업이 즉시 호출됩니다. 따라서 서명자에게 보내는 Adobe Sign 계약 PDF는 제출 작업에서 사용하거나 처리할 수 없습니다. (FORM_SIGN_INTEGRATION)

* 서명 단계를 사용할 수 없습니다. (SIGNATURE_STEP)

* 확인 단계를 사용할 수 없습니다. (VERIFY_STEP)

* Forms 포털 기능 및 **[!UICONTROL Forms Portal 제출 작업]**&#x200B;은 아직 사용할 수 없습니다. (FORMS._PORTAL_SUBMISSION, FORMS._PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* **[!UICONTROL Forms Workflow]**&#x200B;제출 작업을 사용할 수 없습니다. [!DNL AEM 6.5 Forms] 및 이전 버전에서 제출 작업은 기존 [!DNL AEM Forms on JEE] 워크플로우 및 LiveCycle Workflow에 적응형 양식 데이터를 제출하는 데 사용되었습니다. (LC_WORKFLOW_SUBMISSION)

* 대화형 통신 기능을 사용할 수 없습니다.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL 다른 이름으로]** 저장 및  **[!UICONTROL 자동]** 저장 적응형 양식 기능은 현재 지원되지 않습니다. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* 메타데이터 아코디언을 사용할 수 없습니다. (METADATA_ACCORDION_FORM_CONTAINER)

* 이제 CAPTCHA 구성 요소는 Google reCAPTCHA 서비스를 사용하여 CAPTCHA의 유효성을 확인합니다. Adobe Experience Manager을 사용하여 CAPTCHA의 유효성을 검사하는 옵션은 더 이상 사용되지 않습니다. (FORMS._CAPTCHA)

* [!DNL AEM Forms] 앱을 사용할 수 없습니다  [!DNL Cloud Services]. (AEM_FORMS._APP)

* [문서 ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) 서비스 단계는 AEM 워크플로우에서 사용할 수 없습니다. (WORKFLOW_DOCSERVICES)

## 가능한 솔루션 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="구현 지침"
>abstract="FORMS을 통해 노출된 정보. 코드는 일부 기능 및 API가 Cloud Service과 호환되도록 하는 데 필요한 대체 및 기타 작업에 대한 지침을 제공할 수 있습니다. 도움말 및 분류에 대한 Adobe 지원 센터에 문의하십시오"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 마이그레이션 유틸리티를 사용하여 환경에 있는 모든 규칙 스크립트를 재사용 가능한 기능으로 변환합니다. 시각적 규칙 편집기와 함께 재사용 가능한 함수를 사용하여 규칙 스크립트로 얻은 결과를 계속 얻을 수 있습니다. (CODE_EDITOR)

* 환경에 대해 전자 메일(SMTP 포트 열기) 기능을 활성화하려면 지원 팀에 문의하십시오. 기본적으로 나가는 HTTP 및 HTTPS 연결만 활성화됩니다. (EMAIL_SERVICE_CONFIGURATION, 이메일 단계)

* **[!UICONTROL 전자 메일 PDF]** 대신 **[!UICONTROL 전자 메일]** 제출 작업을 사용하십시오. **[!UICONTROL 전자 메일]** 제출 작업은 첨부 파일을 보내고 전자 메일에 레코드 문서(DoR)를 첨부하는 옵션을 제공합니다. (EMAIL_PDF_SUBMIT_ACTION)

* 제출된 데이터에 Adobe Sign 계약 ID가 포함되어 있습니다. 필요한 경우 서명 계약 ID를 사용하여 서명 계약 PDF를 검색할 수 있습니다.  (FORM_SIGN_INTEGRATION)

* 기존 적응형 양식에서 서명 단계를 제거합니다. 브라우저 내 서명 경험](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684)을 사용하도록 적응형 양식을 구성합니다. [ 적응형 양식 제출 시 브라우저 내에서 계약에 서명하도록 Adobe Sign 계약이 표시됩니다. 브라우저 내 서명 환경은 더욱 빠른 서명 경험을 제공하고 서명자를 위한 시간을 절약합니다. (SIGNATURE_STEP)

* 기존 적응형 Forms에서 확인 단계를 제거하고 이러한 양식을 [!DNL Cloud Service] 환경으로 이동합니다. (VERIFY_STEP)

* 기존 적응형 양식을 수정하여 [REST 엔드포인트에 제출](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [이메일 보내기](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [양식 데이터 모델](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) 및 [AEM 워크플로우 호출](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) 작업 제출을 사용합니다. Forms 포털 및 Forms 포털 제출 작업은 아직 사용할 수 없습니다. 기능 가용성에 대한 자세한 내용은 월별 릴리스 노트를 참조하십시오. (FORMS._PORTAL_SUBMISSION, FORMS._PORTAL)

* AEM 워크플로우를 개발하고 기존 적응형 양식을 수정하여 [AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) 작업을 사용하여 **[!UICONTROL Forms Workflow에 제출]** 작업 제출을 사용하는 대신 데이터를 AEM Workflow에 보낼 수 있습니다. [!UICONTROL Forms Workflow에 제출]을 사용하는 대신 LiveCycle 프로세스에 데이터, 첨부 파일 또는 레코드 문서(DoR)를 전송하는 사용자 지정 제출 작업을 개발할 수 있습니다. (LC_WORKFLOW_SUBMISSION)

* 대화형 통신 기능 가용성에 대한 자세한 내용은 월별 릴리스 노트를 참조하십시오. 기능을 사용할 수 없을 때까지 대화형 통신, 문자 및 관련 사전을 Cloud Service 환경으로 마이그레이션하지 마십시오. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Cloud Service으로 마이그레이션하기 전에 적응형 Forms에서 **[!UICONTROL 초안]** 및 **[!UICONTROL 자동 저장 활성화]** 옵션을 비활성화합니다. Cloud Service에 대해 Forms 포털 기능이 릴리스되면 이러한 옵션을 활성화할 수 있습니다. 기능 가용성에 대한 자세한 내용은 월별 릴리스 노트를 참조하십시오. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* 메타데이터 아코디언을 대체할 수 없습니다. Cloud Service으로 마이그레이션하기 전에 양식에서 제거하십시오.(METADATA_ACCORDION_FORM_CONTAINER)

* Adobe Experience Manager에서 제공하는 CAPTCHA 서비스 대신 Google reCaptcha를 사용하십시오. (FORMS._CAPTCHA)

* 적응형 Forms은 반응형 디자인을 제공합니다. 이러한 양식은 기본 장치를 기반으로 모양, 디자인 및 상호 작용을 변경합니다. 모바일 장치에서 응용 Forms을 계속 사용할 수 있습니다. [!DNL AEM Forms] 앱의 가용성에 대한 정보는 월별 릴리스 노트를 찾습니다. (AEM_FORMS._APP)

* 문서 서비스 워크플로우 단계를 사용하는 AEM 워크플로우 모델을 마이그레이션하지 마십시오. 또한 양식을 마이그레이션하기 전에 Document Services 워크플로우 단계를 사용하는 워크플로우 모델로 사용자 데이터를 보내는 적응형 Forms을 마이그레이션하거나 업데이트하거나 제출 작업을 [지원되는 하나](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html)로 변경하지 마십시오. (WORKFLOW_DOCSERVICES)

* XFA 기반 응용 Forms에 대한 지원은 즉시 사용할 수 없습니다. XFA 기반 적응형 Forms을 사용하려면 사용 사례 및 특정 요구 사항에 대한 자세한 내용을 보려면 Adobe 지원 센터에 문의하십시오.(XFA_BASED_FORM, XDP_BASED_FORM)

[Adobe 지원](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html)에 연락하여 명확히 하거나 문제를 해결하십시오.
