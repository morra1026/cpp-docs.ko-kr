---
title: Microsoft 전용 한정자
ms.date: 08/16/2018
ms.assetid: 22c7178c-f854-47fa-9de6-07d23fda58e1
ms.openlocfilehash: be126e90ca6f77ef43b49ccd5b83c0f307f7f307
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50646032"
---
# <a name="microsoft-specific-modifiers"></a>Microsoft 전용 한정자

이 단원에서는 다음 영역의 Microsoft 전용 C++ 확장에 대해 설명합니다.

- [기반 주소](based-addressing.md)에 대 한 포인터를 사용 하 여 다른 포인터가 오프셋 하는 데 사용 될 수 있는 기준으로 하는 방법

- [함수 호출 규칙](calling-conventions.md)

- 확장 저장소 클래스 특성을 사용 하 여 선언 된 [__declspec](declspec.md) 키워드

- 합니다 [__w64](w64.md) 키워드

## <a name="microsoft-specific-keywords"></a>Microsoft 전용 키워드

Microsoft 전용 키워드 중 대다수는 파생 형식을 형성하는 선언자를 수정하는 데 사용될 수 있습니다. 선언 자에 대 한 자세한 내용은 참조 하세요. [선언 자](overview-of-declarators.md)합니다.

|키워드|의미|파생 형식을 만드는 데 사용됩니까?|
|-------------|-------------|---------------------------------|
|[__based](based-grammar.md)|뒤에 오는 이름이 32비트 오프셋을 선언에 포함된 32비트 기준으로 선언합니다.|예|
|[__cdecl](cdecl.md)|뒤에 오는 이름이 C 명명 및 호출 규칙을 사용합니다.|예|
|[__declspec](declspec.md)|뒤에 오는 이름이 Microsoft 전용 저장소 클래스 특성을 지정합니다.|아니요|
|[__fastcall](fastcall.md)|뒤에 오는 이름이 인수 전달 시 가능하면 스택 대신 레지스터를 사용하는 함수를 선언합니다.|예|
|[__restrict](extension-restrict.md)|__Declspec 비슷합니다 ([제한](restrict.md)), 하지만 변수에서 사용 합니다.|아니요|
|[__stdcall](stdcall.md)|뒤에 오는 이름이 표준 호출 규칙을 준수하는 함수를 지정합니다.|예|
|[__w64](w64.md)|64비트 컴파일러에서 더 큰 형식으로 데이터 형식을 표시합니다.|아니요|
|[__unaligned](unaligned.md)|형식 또는 다른 데이터의 포인터가 정렬되지 않음을 지정합니다.|아니요|
|[__vectorcall](vectorcall.md)|뒤에 오는 이름이 인수 전달 시 가능하면 스택 대신 SSE 레지스터 등의 레지스터를 사용하는 함수를 선언합니다.|예|

## <a name="see-also"></a>참고 항목

[C++ 언어 참조](cpp-language-reference.md)