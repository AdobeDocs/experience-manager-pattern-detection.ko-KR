---
title: MI
description: 패턴 감지기 코드 도움말 페이지
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: efb06dc7e00f91d4c080553df3153deb90b093f2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 100%

---

# MI {#mi}

구성 오류 문제

## 배경 {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="구성 오류 문제"
>abstract="MI는 AEM 인스턴스에서 구성 문제 식별"

`MI` 구성 오류 문제는 AEM 인스턴스의 구성 문제를 식별합니다.

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
   * 사용 가능한 프로세서의 절반을 사용하려면 값을 0.5로 설정하는 것이 좋습니다.
* `missing.maintenance.configuration`
   * 개정 정리: [개정 정리](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html)를 참조하십시오. 구성과 관련된 중요한 부분은 [개정 정리 - 테일 및 전체 압축 구성](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction)에 있습니다.
   * Lucene 바이너리 정리: [작업 대시보드 - Lucene 바이너리 정리](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup)를 참조하십시오.
   * 데이터 스토어 가비지 수집: [데이터 스토어 가비지 수집](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html)을 참조하십시오.
   * 워크플로 제거: [정기적인 워크플로 인스턴스 제거](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html#regular-purging-of-workflow-instances)를 참조하십시오.
   * 감사 로그 유지 관리 작업: [감사 로그 유지 관리](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html)를 참조하십시오.
* 자세한 설명이 필요하거나 문제를 해결하려면 [Experience Manager 고객 지원 팀](https://helpx.adobe.com/kr/enterprise/using/support-for-experience-cloud.html)에 문의하십시오.
