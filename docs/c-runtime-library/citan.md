---
title: _CItan
ms.date: 04/11/2018
apiname:
- _CItan
apilocation:
- msvcr100.dll
- msvcr110_clr0400.dll
- msvcr80.dll
- msvcrt.dll
- msvcr110.dll
- msvcr90.dll
- msvcr120.dll
apitype: DLLExport
f1_keywords:
- _CItan
- CItan
helpviewer_keywords:
- CItan intrinsic
- _CItan intrinsic
ms.assetid: d1ea3113-50a2-45a6-b6bc-680fcdcc0928
ms.openlocfilehash: fdefe8674ede78de194fbb884bd2c90fe0a96d06
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50650699"
---
# <a name="citan"></a>_CItan

부동 소수점 스택의 맨 위에 있는 값의 탄젠트를 계산합니다.

## <a name="syntax"></a>구문

```C
void __cdecl _CItan();
```

## <a name="remarks"></a>설명

이 버전의 [tan](../c-runtime-library/reference/tan-tanf-tanl.md) 함수에는 컴파일러에서 인식할 수 있는 특별한 호출 규칙이 있습니다. 이 함수는 복사본이 생성되지 않도록 하며 레지스터 할당을 돕기 때문에 실행 속도를 높입니다.

결과 값이 부동 소수점 스택의 맨 위에 푸시됩니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** x86

## <a name="see-also"></a>참고 항목

[사전순 함수 참조](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[tan, tanf, tanl](../c-runtime-library/reference/tan-tanf-tanl.md)<br/>
