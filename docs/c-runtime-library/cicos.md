---
title: _CIcos
ms.date: 04/11/2018
apiname:
- _CIcos
apilocation:
- msvcr90.dll
- msvcrt.dll
- msvcr120.dll
- msvcr100.dll
- msvcr80.dll
- msvcr110_clr0400.dll
- msvcr110.dll
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- CIcos
- _CIcos
helpviewer_keywords:
- _CIcos intrinsic
- CIcos intrinsic
ms.assetid: 6fc203fb-66f3-4ead-9784-f85833c26f1b
ms.openlocfilehash: fef9ef9e197dcd6e8a1880c3acdfa2755ccf1ae1
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702728"
---
# <a name="cicos"></a>_CIcos

부동 소수점 스택의 맨 위에 있는 값의 코사인을 계산합니다.

## <a name="syntax"></a>구문

```C
void __cdecl _CIcos();
```

## <a name="remarks"></a>주의

이 버전의 [cos](../c-runtime-library/reference/cos-cosf-cosl.md) 함수에는 컴파일러에서 인식할 수 있는 특별한 호출 규칙이 있습니다. 복사본이 생성되지 않도록 하며 레지스터 할당을 돕기 때문에 실행 속도를 높입니다.

결과 값이 부동 소수점 스택의 맨 위에 푸시됩니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** x86

## <a name="see-also"></a>참고 항목

[사전순 함수 참조](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[cos, cosf, cosl](../c-runtime-library/reference/cos-cosf-cosl.md)<br/>
