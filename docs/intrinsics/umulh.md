---
title: __umulh | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __umulh
dev_langs:
- C++
helpviewer_keywords:
- __umulh intrinsic
ms.assetid: d241b53a-e6f7-4af1-9f6e-84e149158f03
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 840dc430189a81108d92aa692e7e5b9845375910
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46430828"
---
# <a name="umulh"></a>__umulh

**Microsoft 전용**

64비트 부호 없는 두 정수의 곱에서 상위 64비트를 반환합니다.

## <a name="syntax"></a>구문

```
unsigned __int64 __umulh( 
   unsigned __int64 a, 
   unsigned __int64 b 
);
```

#### <a name="parameters"></a>매개 변수

*a*<br/>
[in] 곱할 첫 번째 숫자입니다.

*b*<br/>
[in] 곱할 두 번째 숫자입니다.

## <a name="return-value"></a>반환 값

곱셈의 128비트 결과에서 상위 64비트입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__umulh`|X64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이러한 루틴은 내장 함수로만 사용할 수 있습니다.

## <a name="example"></a>예제

```
// umulh.cpp
// processor: X64
#include <cstdio>
#include <intrin.h>

int main()
{
    unsigned __int64 i = 0x10;
    unsigned __int64 j = 0xFEDCBA9876543210;
    unsigned __int64 k = i * j; // k has the low 64 bits
                                // of the product.
    unsigned __int64 result;
    result = __umulh(i, j); // result has the high 64 bits
                            // of the product.
    printf_s("0x%I64x * 0x%I64x = 0x%I64x%I64x \n", i, j, result, k);
    return 0;
}
```

```Output
0x10 * 0xfedcba9876543210 = 0xfedcba98765432100
```

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)