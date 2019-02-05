---
title: _CIatan2
ms.date: 11/04/2016
apiname:
- _CIatan2
apilocation:
- msvcr80.dll
- msvcrt.dll
- msvcr120.dll
- msvcr110_clr0400.dll
- msvcr110.dll
- msvcr100.dll
- msvcr90.dll
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- CIatan2
- _CIatan2
helpviewer_keywords:
- _CIatan2 intrinsic
- CIatan2 intrinsic
ms.assetid: 31f8cc78-b79f-4576-b73b-8add18e08680
ms.openlocfilehash: a09bc8af5ab6ef6d99efea8448098d1a2f03d580
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55703261"
---
# <a name="ciatan2"></a>_CIatan2

*x* 및 *y*가 스택의 맨 위에 있는 값인 경우 *x* / *y*의 아크탄젠트를 계산합니다.

## <a name="syntax"></a>구문

```
void __cdecl _CIatan2();
```

## <a name="remarks"></a>주의

이 버전의 `atan2` 함수는 컴파일러가 이해할 수 있는 특별한 호출 규칙을 가집니다. 복사본이 생성되지 않도록 하며 레지스터 할당을 돕기 때문에 실행 속도를 높입니다.

결과 값이 스택의 맨 위에 푸시됩니다.

## <a name="requirements"></a>요구 사항

**플랫폼:** x86

## <a name="see-also"></a>참고 항목

[사전순 함수 참조](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[atan, atanf, atanl, atan2, atan2f, atan2l](../c-runtime-library/reference/atan-atanf-atanl-atan2-atan2f-atan2l.md)