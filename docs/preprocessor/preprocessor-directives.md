---
title: 전처리기 지시문 | Microsoft Docs
ms.custom: ''
ms.date: 06/28/2018
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- directives, preprocessor
- preprocessor, directives
ms.assetid: e0fc4564-b6cf-4a36-bf51-6ccd7abd0a94
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7e218002171b7ad2d141be227ab277851487f0f5
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43678802"
---
# <a name="preprocessor-directives"></a>전처리기 지시문

전처리기 지시문과 같은 `#define` 및 `#ifdef`는 일반적으로 변경 하 고 여러 실행 환경에서 컴파일하는 데 쉽습니다 소스 프로그램을 확인 하는 데 사용 됩니다. 소스 파일의 지시문은 특정 작업을 수행하도록 전처리기에 지시합니다. 예를 들어 전처리기는 텍스트에서 토큰을 바꾸거나, 다른 파일의 내용을 소스 파일에 삽입하거나, 텍스트 섹션을 제거하여 파일 일부의 컴파일을 억제할 수 있습니다. 전처리기 코드 줄은 매크로 확장 전에 인식되고 수행됩니다. 따라서 매크로가 전처리기 명령처럼 보이는 항목으로 확장되는 경우 해당 명령은 전처리기에서 인식되지 않습니다.

전처리기 문은 이스케이프 시퀀스가 지원되지 않는 것을 제외하고 소스 파일 문과 동일한 문자 집합을 사용합니다. 전처리기 문에 사용된 문자 집합은 실행 문자 집합과 동일합니다. 전처리기는 음수 문자 값도 인식합니다.

전처리기는 다음 지시문을 인식합니다.

|||||
|-|-|-|-|
|[#define](../preprocessor/hash-define-directive-c-cpp.md)|[#error](../preprocessor/hash-error-directive-c-cpp.md)|[#import](../preprocessor/hash-import-directive-cpp.md)|[#undef](../preprocessor/hash-undef-directive-c-cpp.md)|
|[#elif](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md)|[#if](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md)|[#include](../preprocessor/hash-include-directive-c-cpp.md)|[#using](../preprocessor/hash-using-directive-cpp.md)|
|[#else](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md)|[#ifdef](../preprocessor/hash-ifdef-and-hash-ifndef-directives-c-cpp.md)|[#line](../preprocessor/hash-line-directive-c-cpp.md)|[#endif](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md)|
|[#ifndef](../preprocessor/hash-ifdef-and-hash-ifndef-directives-c-cpp.md)|[#pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)|||

숫자 기호 (**#**) 해야 합니다; 지시문이 포함 된 줄에서 첫 번째 공백이 아닌 문자 수 공백 문자는 숫자 기호와 지시문의 첫 문자 사이 나타날 수 있습니다. 일부 지시문에는 인수 또는 값이 포함됩니다. 인수 또는 지시문의 일부인 값) (제외 지시문 뒤에 오는 모든 텍스트 줄으로 된 주석 구분 기호 뒤에 야 (**//**)로 묶여야 주석 구분 기호 ( __/ \*\*/__). 전처리기 지시문이 포함 된 줄 바로 앞에 백슬래시를 사용 하 여 줄의 끝 표식에서 계속할 수 있습니다 (**\\**).

전처리기 지시문은 소스 파일의 어느 곳에나 나타날 수 있지만 소스 파일의 나머지 부분에만 적용됩니다.

## <a name="see-also"></a>참고자료

[전처리기 연산자](../preprocessor/preprocessor-operators.md)  
[미리 정의된 매크로](../preprocessor/predefined-macros.md)  
[ 전처리기 참조](../preprocessor/c-cpp-preprocessor-reference.md)  
