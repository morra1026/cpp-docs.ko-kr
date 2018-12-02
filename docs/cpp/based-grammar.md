---
title: __based 문법
ms.date: 11/04/2016
helpviewer_keywords:
- based addressing
ms.assetid: a68ff750-c7fa-4c0c-8d5f-2df76e4686c5
ms.openlocfilehash: 8dec9b0bcc7db25e2ec4c39b9d907922691bfc05
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50558147"
---
# <a name="based-grammar"></a>__based 문법

## <a name="microsoft-specific"></a>Microsoft 전용

기반 주소 지정은 개체가 할당된(정적 및 동적 기반 데이터) 세그먼트를 정밀하게 제어해야 할 때 유용합니다.

32비트 및 64비트 컴파일러에서 허용되는 기반 주소 지정의 유일한 형식은 32비트 또는 64비트 기반으로의 32비트 또는 64비트의 치환을 포함하는 형식을 정의, 또는 **void**에 기초한 "포인터 기반"입니다.    
  
## <a name="grammar"></a>문법

*based-range-modifier*: **__based (***base-expression***)** 

*base-expression*: *based-variablebased-abstract-declaratorsegment-namesegment-cast*

*based-variable*: *identifier*

*based-abstract-declarator*: *abstract-declarator*

*base-type*: *type-name*

**Microsoft 전용 종료**

## <a name="see-also"></a>참고

[기반 포인터](../cpp/based-pointers-cpp.md)
