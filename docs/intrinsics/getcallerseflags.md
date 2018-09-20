---
title: __getcallerseflags | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- _getcallerseflags
- _getcallerseflags_cpp
dev_langs:
- C++
helpviewer_keywords:
- _getcallerseflags intrinsic
ms.assetid: 2386596f-33aa-4cc7-b026-5a834637270a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4f16079fce7bda86a376baf783db8b05ec098015
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46410197"
---
# <a name="getcallerseflags"></a>__getcallerseflags

**Microsoft 전용**

호출자의 컨텍스트에서 EFLAGS 값을 반환합니다.

## <a name="syntax"></a>구문

```
unsigned int __getcallerseflags(void);
```

## <a name="return-value"></a>반환 값

호출자의 컨텍스트에서 EFLAGS 값입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__getcallerseflags`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

이 루틴은 내장 루틴으로만 사용할 수 있습니다.

## <a name="example"></a>예제

```
// getcallerseflags.cpp
// processor: x86, x64

#include <stdio.h>
#include <intrin.h>

#pragma intrinsic(__getcallerseflags)

unsigned int g()
{
    unsigned int EFLAGS = __getcallerseflags();
    printf_s("EFLAGS 0x%x\n", EFLAGS);
    return EFLAGS;
}
unsigned int f()
{
    return g();
}

int main()
{
    unsigned int i;
    i = f();
    i = g();
    return 0;
}
```

```Output
EFLAGS 0x202
EFLAGS 0x206
```

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)