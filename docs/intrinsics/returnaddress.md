---
title: _ReturnAddress | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _ReturnAddress
dev_langs:
- C++
helpviewer_keywords:
- _ReturnAddress intrinsic
- ReturnAddress intrinsic
ms.assetid: 7f4a5811-35e6-4f64-ba7c-21203380eeda
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5c739590e5e208d9f83fa059f191ae80612a0dbd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46380876"
---
# <a name="returnaddress"></a>_ReturnAddress

## <a name="microsoft-specific"></a>Microsoft 전용

`_ReturnAddress` 내장 컨트롤 호출자에 게 반환 된 후 실행 되는 함수 호출에서 명령의 주소를 제공 합니다.

다음 프로그램 및 디버거에서 단계별로 진행을 빌드하십시오. 프로그램을 단계별로 확인에서 반환 되는 주소 `_ReturnAddress`합니다. 함수에서 반환 된 후 즉시 다음 여기서 `_ReturnAddress` 사용 되는, 열기를 [방법: 디스어셈블리 창을 사용 하 여](/visualstudio/debugger/how-to-use-the-disassembly-window) 다음 명령 실행할 주소의 를반환하는주소와일치하는지확인`_ReturnAddress`.

인라인 월 같은 최적화 반송 주소에 영향을 줍니다. 예를 들어 아래 샘플 프로그램을 사용 하 여 컴파일된 [/Ob1](../build/reference/ob-inline-function-expansion.md)를 `inline_func` 호출 하는 함수를 인라인 처리 되지 `main`합니다. 따라서 호출 `_ReturnAddress` 에서 `inline_func` 고 `main` 동일한 값이 각 생성 됩니다.

때 `_ReturnAddress` 로 컴파일된 프로그램에서 사용 됩니다 [/clr](../build/reference/clr-common-language-runtime-compilation.md)를 포함 하는 함수는 `_ReturnAddress` 네이티브 함수로 호출 컴파일됩니다. 포함 하는 함수에 대 한 호출은 관리 되는 함수를 컴파일할 때 `_ReturnAddress`, `_ReturnAddress` 예상 대로 작동 하지 않을 수 있습니다.

## <a name="requirements"></a>요구 사항

**헤더 파일** \<intrin.h >

## <a name="example"></a>예제

```
// compiler_intrinsics__ReturnAddress.cpp
#include <stdio.h>
#include <intrin.h>

#pragma intrinsic(_ReturnAddress)

__declspec(noinline)
void noinline_func(void)
{
   printf("Return address from %s: %p\n", __FUNCTION__, _ReturnAddress());
}

__forceinline
void inline_func(void)
{
   printf("Return address from %s: %p\n", __FUNCTION__, _ReturnAddress());
}

int main(void)
{
   noinline_func();
   inline_func();
   printf("Return address from %s: %p\n", __FUNCTION__, _ReturnAddress());

   return 0;
}
```

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[_AddressOfReturnAddress](../intrinsics/addressofreturnaddress.md)<br/>
[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[키워드](../cpp/keywords-cpp.md)