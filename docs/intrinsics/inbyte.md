---
title: __inbyte
ms.date: 11/04/2016
f1_keywords:
- __inbyte
- __inbyte_cpp
helpviewer_keywords:
- in instruction
- __inbyte intrinsic
ms.assetid: 03b61799-2a08-474d-adc4-2cbf7c81a4d5
ms.openlocfilehash: 63d4e9229eb7c5058587975d0ea04696786a9c73
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50562151"
---
# <a name="inbyte"></a>__inbyte

**Microsoft 전용**

생성 된 `in` 명령 1 바이트를 반환 하 여 지정 된 포트에서 읽은 `Port`합니다.

## <a name="syntax"></a>구문

```
unsigned char __inbyte(
   unsigned short Port
);
```

#### <a name="parameters"></a>매개 변수

*포트*<br/>
[in] 포트에서 읽기입니다.

## <a name="return-value"></a>반환 값

지정된 된 포트에서 읽은 바이트입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__inbyte`|x86, x64|

**헤더 파일** \<intrin.h >

**Microsoft 전용 종료**

## <a name="remarks"></a>설명

이 루틴은 내장 루틴으로만 사용할 수 있습니다.

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)