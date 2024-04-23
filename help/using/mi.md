---
title: MI
description: 패턴 감지기 코드 도움말 페이지
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 54%

---

# MI {#mi}

구성 오류 문제

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="구성 오류 문제"
>abstract="MI는 AEM 인스턴스에서 구성 문제 식별"

MI 잘못된 구성 문제가 AEM 인스턴스의 구성 문제를 식별합니다.

다양한 유형의 정보 식별을 위해 다음과 같은 하위 유형이 사용됩니다.

* `sling.job.max.parallel`: 최대 병렬 구성이 -1로 설정된 Sling 작업을 식별합니다.
* `missing.maintenance.configuration`: 누락된 유지 관리 작업 구성을 식별합니다.

## 가능한 영향 및 위험 {#implications-and-risks}

* `sling.job.max.parallel`
   * 값 -1은 사용 가능한 프로세서 수로 대체됩니다. 이로 인해 AEM 인스턴스에서 성능 문제가 발생할 수 있습니다.
* `missing.maintenance.configuration`
   * 유지 관리 작업 구성이 누락되면 성능이 저하되거나 인스턴스가 손상될 수 있습니다.

## 가능한 해결 방법 {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="구현 지침"
>abstract="도움이 필요한 경우 고객 지원 센터에 문의하십시오."
>additional-url="https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html" text="Experience Cloud 지원"

* `sling.job.max.parallel`
   * Adobe은 사용 가능한 프로세서의 절반을 활용하려면 값을 0.5로 설정하는 것이 좋습니다.
* `missing.maintenance.configuration`
   * 개정 정리: 참조 [개정 정리](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). 구성과 관련된 중요한 부분은 [개정 정리 - 테일 및 전체 압축 구성](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup)에 있습니다.
   * Lucene 바이너리 정리: 다음을 참조하십시오. [작업 대시보드 - Lucene 바이너리 정리](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * 데이터 저장소 가비지 수집: 참조 [데이터 저장소 가비지 수집](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * 워크플로우 삭제: 참조 [정기적인 워크플로 인스턴스 제거](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * AuditLog 유지 관리 작업: 을 참조하십시오. [감사 로그 유지 관리](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* 다음으로 문의: [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html) 설명 또는 문제 해결을 위해.
