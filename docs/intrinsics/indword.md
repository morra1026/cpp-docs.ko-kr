---
title: __indword
ms.date: 11/04/2016
f1_keywords:
- __indword_cpp
- __indword
helpviewer_keywords:
- in instruction
- __indword intrinsic
ms.assetid: 1068d686-586e-4e36-b962-d1d7c3315260
ms.openlocfilehash: f4b37247093da14c8d5e8fed69b01265d3fed2ee
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50599812"
---
# <a name="indword"></a>__indword

**Microsoft 전용**

데이터의 2 배 워드를 하나 사용 하 여 지정 된 포트에서 읽기를 `in` 명령입니다.

## <a name="syntax"></a>구문

```
unsigned long __indword(
   unsigned short Port
);
```

#### <a name="parameters"></a>매개 변수

*포트*<br/>
[in] 포트에서 읽기입니다.

## <a name="return-value"></a>반환 값

단어 포트에서 읽습니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__indword`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 루틴은 내장 루틴으로만 사용할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)