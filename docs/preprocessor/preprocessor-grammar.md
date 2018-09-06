---
title: 전처리기 문법 | Microsoft Docs
ms.custom: ''
ms.date: 09/04/2018
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- preprocessor
- grammar, preprocessor
- preprocessor, grammar
ms.assetid: 6cd33fad-0b08-4592-9be8-7359c43e24e9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 56df4d0bfdaf87ace87a9f9dcbde85166929e642
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43766118"
---
# <a name="preprocessor-grammar"></a>전처리기 문법

*컨트롤 줄*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#define** *식별자* *토큰 문자열*<sub>최적화</sub><br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#define** <em>식별자</em>**(** *식별자*<sub>opt</sub> **,** ... **하십시오** *식별자*<sub>opt</sub> **)** *토큰 문자열*<sub>최적화</sub><br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#include** **"** *경로-사양* **"**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#include** **\<** *경로-사양* **>**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#line** *숫자 시퀀스***"** *filename* **"**<sub>최적화  </sub><br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#undef** *식별자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#error** *토큰 문자열*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#pragma** *토큰 문자열*

*constant-expression*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**정의 (** *식별자* **)**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**정의** *식별자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;다른 상수 식

*조건부* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*경우 부작* *elif 부분*<sub>opt</sub> *else 부분*<sub>opt</sub> *endif 줄*

*if-part* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*경우에 아웃오브 라인* *텍스트*

*if-line* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#if** *상수 식*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#ifdef** *식별자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#ifndef** *식별자*

*elif-parts* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*elif 줄* *텍스트*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*elif 부분* *elif 아웃오브 라인* *텍스트*

*elif-line* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#elif** *상수 식*

*else-part* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*다른 줄* *텍스트*

*else-line* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#else**

*endif-line* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**#endif**

*digit-sequence* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*숫자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*숫자 시퀀스* *숫자*

*숫자* : 중<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**0 1 2 3 4 5 6 7 8 9**

*token-string* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;토큰 문자열

*token* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*키워드*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*식별자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*상수*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*연산자*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*문장 부호*

*filename* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;올바른 운영 체제 파일 이름

*path-spec* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;올바른 파일 경로

*텍스트* :<br/>
&nbsp;&nbsp;&nbsp;&nbsp;임의의 텍스트 시퀀스

> [!NOTE]
> 다음 비 단말에는 확장 되어는 [어휘 규칙](../cpp/lexical-conventions.md) 섹션을 *c + + 언어 참조*: *상수*, *상수 식* , *식별자*합니다 *키워드*를 *연산자*, 및 *문장 부호*합니다.

## <a name="see-also"></a>참고 항목

[문법 요약(C/C++)](../preprocessor/grammar-summary-c-cpp.md)