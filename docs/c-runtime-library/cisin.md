---
title: _CIsin
ms.date: 04/10/2018
apiname:
- _CIsin
apilocation:
- msvcr80.dll
- msvcr100.dll
- msvcrt.dll
- msvcr110.dll
- msvcr120.dll
- msvcr90.dll
- msvcr110_clr0400.dll
apitype: DLLExport
f1_keywords:
- CIsin
- _CIsin
helpviewer_keywords:
- _CIsin intrinsic
- CIsin intrinsic
ms.assetid: f215f39a-2341-4f1c-ba8e-cb522451ceb2
ms.openlocfilehash: 89350cdc61b7c96b09242731f89c934727e44a19
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50481306"
---
# <a name="cisin"></a>_CIsin

부동 소수점 스택의 맨 위에 있는 값의 사인을 계산합니다.

## <a name="syntax"></a>구문

```C
void __cdecl _CIsin();
```

## <a name="remarks"></a>설명

이 버전의 [sin](../c-runtime-library/reference/sin-sinf-sinl.md) 함수에는 컴파일러에서 인식할 수 있는 특별한 호출 규칙이 있습니다. 복사본이 생성되지 않도록 하며 레지스터 할당을 돕기 때문에 실행 속도를 높입니다.

결과 값이 부동 소수점 스택의 맨 위에 푸시됩니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** x86

## <a name="see-also"></a>참고 항목

[사전순 함수 참조](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[sin, sinf, sinl](../c-runtime-library/reference/sin-sinf-sinl.md)<br/>
