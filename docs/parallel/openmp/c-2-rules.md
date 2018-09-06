---
title: C.2 규칙 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 4d52fef7-3eb7-4480-a335-8ed48681092b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: bb83b35a03608e272e9af67159b61e5dbf4e1ec6
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43755023"
---
# <a name="c2-rules"></a>C.2 규칙
표기법은 6.1 C 표준의 섹션에 설명 되어 있습니다. 이 문법 부록 OpenMP C 및 c + + 지시문에 대 한 기본 언어 문법을 확장을 보여 줍니다.

**/\* c + + (ISO/IEC 14882:1998) \*/**

*문-seq*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*openmp 지시문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문-seq 문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문-seq openmp 지시문*

**/\* C90에서 (ISO/IEC 9899:1990) \*/**

*statement-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*openmp 지시문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문 목록 문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문 목록 openmp 지시문*

**/\* C99에서 (ISO/IEC 9899:1999) \*/**

*항목 차단*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*선언*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*openmp 지시문*

**/\* 표준 문 \*/**

*statement*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*openmp 생성자*

*openmp 구문을*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*병렬 구문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*구문에 대 한*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*섹션 구문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*단일 생성자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*구문에 대 한 병렬*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*병렬 섹션 생성자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*master 구문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*critical 구문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*atomic 구문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*순서가 지정 된 생성자*

*openmp 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*barrier 지시문*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*flush 지시문*

*구조화 된 블록*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문*

*병렬 구문을*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*병렬 지시문 구조화 된 블록*

*병렬 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp** *병렬 절*<sub>optseq</sub> *줄 바꿈*

*병렬 절*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*고유 병렬 절*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*데이터 절*

*병렬 절 고유*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**경우 (** *식을* **)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**num_threads (** *식을* **)**

*구문에 대 한*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*지시문에 대 한 반복 문*

*지시문에 대 한*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**에 대 한 # pragma omp** *for 절*<sub>optseq</sub> *줄 바꿈*

*for 절*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*절에 대 한 고유*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*데이터 절*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**nowait**

*절에 대 한 고유*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**정렬**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**일정 (** *예약 종류가* **)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**일정 (** *예약 종류가* **하십시오** *식* **)**

*예약 종류가*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**정적**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**동적**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**문제 해결**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**런타임**

*섹션 구문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*섹션 지시문 섹션 범위*

*섹션 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp 섹션** *절 섹션*<sub>optseq</sub> *줄 바꿈*

*섹션 절*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*데이터 절*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**nowait**

*섹션 범위*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*{0} 섹션 시퀀스}*

*섹션 시퀀스*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*섹션 지시문*<sub>opt</sub> *구조화 된 블록*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*섹션 시퀀스 섹션 지시문 구조화 된 블록*

*섹션 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp** *줄 바꿈*

*단일 생성자*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*단일 지시문 구조화 된 블록*

*단일 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**단일 # pragma omp** *단일 절*<sub>optseq</sub> *줄 바꿈*

*단일 절*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*데이터 절*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**nowait**

*구문에 대 한 병렬*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*지시문에 대 한 병렬 반복 문*

*지시문에 대 한 병렬*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**에 대 한 병렬 # pragma omp** *절에 대 한 병렬*<sub>optseq</sub> *줄 바꿈*

*절에 대 한 병렬*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*고유 병렬 절*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*절에 대 한 고유*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*데이터 절*

*병렬 섹션 생성자*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*병렬 섹션 지시문 섹션 범위*

*병렬 섹션 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp 병렬 섹션** *병렬 섹션 절*<sub>optseq</sub> *줄 바꿈*

*절-병렬-섹션*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*고유 병렬 절*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*데이터 절*

*마스터 구문을*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*master 지시문 구조화 된 블록*

*master 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp 마스터** *줄 바꿈*

*critical 구문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*critical 지시문 구조화 된 블록*

*critical 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**중요 한 # pragma omp** *지역 구*<sub>opt</sub> *줄 바꿈*

*지역 구*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*(식별자)*

*barrier 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp 장벽** *줄 바꿈*

*atomic 구문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*원자성 지시문 식 문*

*원자성 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp atomic** *줄 바꿈*

*flush 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp 플러시** *플러시 변수*<sub>opt</sub> *줄 바꿈*

*플러시 변수*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*(변수 목록)*

*순서가 지정 된 구문을*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*순서가 지정 된 지시문 구조화 된 블록*

*순서가 지정 된 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**순서가 지정 된 # pragma omp** *줄 바꿈*

**/\* 표준 선언 \*/**

*선언*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*threadprivate 지시문*

*threadprivate 지시문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**# pragma omp threadprivate (** *변수 목록***)** *줄 바꿈* 

*데이터 절*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**개인 (** *변수 목록* **)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**copyprivate (***변수 목록***)** <br/>
&nbsp;&nbsp;&nbsp;&nbsp;**firstprivate (***변수 목록***)** <br/>
&nbsp;&nbsp;&nbsp;&nbsp;**lastprivate (** *변수 목록***)** <br/>
&nbsp;&nbsp;&nbsp;&nbsp;**공유 (** *변수 목록* **)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**기본 (공유)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**기본값 (없음)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**감소 (***reduction 연산자***:***변수 목록***)** <br/>
&nbsp;&nbsp;&nbsp;&nbsp;**copyin (***변수 목록***)** 

*reduction 연산자*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;중 하나:  **+  \* -& ^ &#124; & &&#124;&#124;**

**/\* C \*/**

*변수 목록*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*식별자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*변수 목록* **하십시오** *식별자*

**/\* c + + \*/**

*변수 목록*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*id 식*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*변수 목록* **하십시오** *id 식*