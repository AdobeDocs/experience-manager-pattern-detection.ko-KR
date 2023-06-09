---
title: FORM
description: 패턴 감지기 코드 도움말 페이지
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 100%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="FORMS 코드는 Adobe Experience Manager Forms에서 Adobe Experience Manager Forms as a Cloud Service로의 마이그레이션과 관련된 잠재적 문제를 식별합니다. 관련된 가능한 영향 및 위험을 검토하여 Cloud Service로 마이그레이션하기 전에 이러한 문제를 해결하십시오."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-pattern-detection/table-of-contents/forms.html#implications-and-risks" text="가능한 영향 및 위험"

`FORMS`는 [!DNL Adobe Experience Manager Forms]에서 [!DNL Adobe Experience Manager Form]s as a [!DNL Cloud Service]로의 마이그레이션과 관련된 잠재적 문제를 식별합니다. [!DNL Cloud Service]로 마이그레이션 하기 전에 이러한 문제를 해결하십시오.

다음 하위 유형은 다양한 유형의 문제를 식별하는 데 도움이 됩니다.

* `modified.feature`: 기능, 에셋 또는 API가 Cloud Service용으로 업데이트 또는 수정되었습니다. Cloud Service로 마이그레이션하기 전에, 마이그레이션 유틸리티를 실행하여 이러한 기능 및 에셋이 Cloud Service와 호환되도록 조정하십시오.
* `unavailable.feature`: 귀하의 환경에 Cloud Service에서 사용 또는 제거할 수 없는 기능 및 에셋이 포함되어 있습니다. 이러한 기능 또는 에셋을 Cloud Service 환경으로 마이그레이션하지 마십시오.
* `unsupported.feature`: 귀하의 환경이 Cloud Service에서 아직 지원되지 않는 일부 기능을 사용합니다. 이러한 기능 또는 에셋을 Cloud Service 환경으로 마이그레이션하지 마십시오. 이들 기능의 가용성에 대한 정보는 월별 릴리스 정보를 확인하십시오.
* `unsupported.api`: 귀하의 환경에 Cloud Service에서 아직 지원되지 않는 일부 API가 포함되어 있습니다. Cloud Service로 마이그레이션하기 전에 귀하의 코드에서 이들 API를 비활성화하고, 바꾸고, 제거하십시오. 이들 기능의 가용성에 대한 정보는 월별 릴리스 정보를 확인하십시오.

일부 기능 및 API를 Cloud Service와 호환되도록 하는 데 필요한 대체 기능 및 기타 작업에 대한 정보는 [가능한 영향 및 위험](#implications-and-risks) 및 [가능한 해결 방법](#solutions) 섹션을 참조하십시오.

## 가능한 영향 및 위험 {#implications-and-risks}

[!DNL Adobe Experience Manager Forms as a Cloud Service]로 마이그레이션 하기 전에 다음 문제를 해결하십시오. 아래에 나열된 영향 및 위험을 해결하지 않으면 일부 기능이 Cloud Service 환경에서 예상한 대로 작동하지 않을 수 있습니다.

* 규칙 편집기 기능의 코드 편집기 기능을 사용할 수 없습니다. (CODE_EDITOR)

* 기본적으로 이메일 지원(SMTP 포트)는 비활성화되어 있습니다. (EMAIL_SERVICE_CONFIGURATION)

* **[!UICONTROL 이메일 PDF]** 제출 액션을 사용할 수 없습니다.(EMAIL_PDF_SUBMIT_ACTION)

* XFA 기반 적응형 양식은 아직 지원되지 않습니다. (XFA_BASED_FORM, XDP_BASED_FORM)

* 모든 서명자가 서명을 완료할 때까지 기다리지 않고 양식 제출에 제출 액션이 즉시 호출됩니다. 따라서 서명자에게 전송된 Adobe Sign 계약서 PDF에 대해 제출 액션을 사용하거나 처리할 수 없습니다. (FORM_SIGN_INTEGRATION)

* 서명 단계를 사용할 수 없습니다. (SIGNATURE_STEP)

* 확인 단계를 사용할 수 없습니다. (VERIFY_STEP)

* **[!UICONTROL Forms Workflow에 제출]** 액션을 사용할 수 없습니다. AEM 6.5 Forms 및 이전 버전에서는 제출 액션을 사용하여 기존 JEE Workflow의 AEM Forms 및 LiveCycle Workflow에 적응형 양식을 제출했습니다. (LC_WORKFLOW_SUBMISSION)

* 대화형 커뮤니케이션 기능을 사용할 수 없습니다. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* 메타데이터 아코디언을 사용할 수 없습니다. (METADATA_ACCORDION_FORM_CONTAINER)

* 이제 CAPTCHA 구성 요소는 기본적으로 Google reCAPTCHA 서비스를 사용하여 CAPTCHA의 유효성을 검사합니다. Adobe Experience Manager를 사용하여 CAPTCHA의 유효성을 검사하는 옵션은 더 이상 사용되지 않습니다. (FORMS_CAPTCHA)

* [!DNL AEM Forms] 앱은 [!DNL Cloud Services]에서 사용할 수 없습니다. (AEM_FORMS_APP)

* [문서 서비스](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=ko#deployment-topology) 단계는 AEM Workflow에서 사용할 수 없습니다. (WORKFLOW_DOCSERVICES)

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="구현 지침"
>abstract="FORMS 코드를 통해 노출된 정보에서 일부 기능 및 API를 Cloud Service와 호환되도록 하는 데 필요한 대체 기능 및 기타 작업에 대한 지침을 얻을 수 있습니다. 도움 및 설명이 필요한 경우 Adobe 지원 팀에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* 마이그레이션 유틸리티를 사용하여 환경의 모든 규칙 스크립트를 재사용 가능한 기능으로 변환하십시오. 재사용 가능한 기능을 시각적 규칙 편집기와 함께 사용하여 규칙 스크립트를 통해 얻은 결과를 유지할 수 있습니다. (CODE_EDITOR)

* 귀하의 환경에 대해 이메일(SMTP 포트 열기) 기능을 활성화하려면 지원 팀에 문의하십시오. 기본적으로 송신 HTTP 및 HTTPS 연결만 활성화할 수 있습니다. (EMAIL_SERVICE_CONFIGURATION, Email step)

* **[!UICONTROL 이메일 PDF]** 대신 **[!UICONTROL 이메일]** 제출 액션을 사용하십시오. **[!UICONTROL 이메일]** 제출 액션은 첨부 파일을 전송하고 이메일에 기록 문서(DoR)를 첨부할 수 있는 옵션을 제공합니다. (EMAIL_PDF_SUBMIT_ACTION)

* 제출된 데이터에는 Adobe Sign Agreement ID가 포함됩니다. 필요한 경우 Sign Agreement ID를 사용하여 Sign Agreement PDF를 가져올 수 있습니다. (FORM_SIGN_INTEGRATION)

* 기존 적응형 양식에서 서명 단계를 제거하십시오. [브라우저 내 서명 경험](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684)을 사용하도록 적응형 양식을 구성하십시오. 브라우저 내 서명 경험은 적응형 양식 제출 시 브라우저 내에 서명할 Adobe Sign 계약서를 표시합니다. 브라우저 내 서명 경험은 서명 속도를 높이고 서명자의 시간을 절약하는 데 도움이 됩니다. (SIGNATURE_STEP)

* 이러한 양식을 [!DNL Cloud Service] 환경으로 이동하기 전에 기존 적응형 양식에서 유효성 검사 단계를 제거하십시오. (VERIFY_STEP)

* [REST 끝점에 제출](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [이메일 전송](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [양식 데이터 모델을 사용하여 제출](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) 및 [AEM Workflow 호출](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) 제출 액션을 사용하도록 기존 적응형 양식을 수정하십시오.

* **[!UICONTROL Forms Workflow에 제출]** 제출 액션을 사용하는 대신 [AEM Workflow](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) 제출 액션을 사용하여 AEM Workflow에 데이터를 전송하도록 AEM Workflow를 개발하고 기존 적응형 양식을 수정할 수 있습니다. [!UICONTROL Forms Workflow에 제출] 액션을 사용하는 대신 LiveCycle 프로세스에 데이터, 첨부 파일 또는 문서 기록을 전송하도록 사용자 지정 제출 액션을 개발할 수 있습니다. (LC_WORKFLOW_SUBMISSION)

* 대화형 커뮤니케이션 기능의 가용성에 대한 정보는 월별 릴리스 정보를 확인하십시오. 해당 기능을 사용할 수 없는 경우 대화형 커뮤니케이션, 문자 및 관련 사전을 Cloud Service 환경으로 마이그레이션할 수 없습니다. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* 메타데이터 아코디언에 대한 대체 기능은 존재하지 않습니다. Cloud Service로 마이그레이션하기 전에 귀하의 양식에서 메타데이터 아코디언을 제거하십시오.(METADATA_ACCORDION_FORM_CONTAINER)

* Adobe Experience Manager에서 제공하는 CAPTCHA 서비스 대신 Google reCaptcha를 사용하십시오. (FORMS_CAPTCHA)

* 문서 서비스 워크플로 단계를 사용하는 AEM Workflow 모델을 마이그레이션하지 마십시오. 또한 문서 서비스 워크플로 단계를 사용하는 워크플로 모델로 사용자 데이터를 전송하는 적응형 양식을 마이그레이션 또는 업데이트하거나 양식을 마이그레이션하기 전에 제출 액션을 [지원되는 액션](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html)으로 변경하지 마십시오. (WORKFLOW_DOCSERVICES)

* 적응형 양식은 반응형 디자인을 제공합니다. 이러한 양식은 기본 디바이스에 따라 모양, 디자인 및 인터랙티브 요소를 변경합니다. 모바일 디바이스에서 적응형 양식을 계속 사용할 수 있습니다. [!DNL AEM Forms] 앱의 가용성에 대한 정보는 월별 릴리스 정보를 확인하십시오. (AEM_FORMS_APP)

* XFA 기반 적응형 양식에 대한 지원은 즉시 사용할 수 없습니다. XFA 기반 적응형 양식을 사용하려는 경우 Adobe 지원 팀에 문의하여 사용 사례 및 특정 요구 사항에 대해 자세히 알아보십시오.(XFA_BASED_FORM, XDP_BASED_FORM)

자세한 설명이 필요하거나 문제를 해결하려면 [Adobe 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
