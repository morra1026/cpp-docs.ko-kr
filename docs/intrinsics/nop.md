---
title: __nop
ms.date: 11/04/2016
f1_keywords:
- __nop
helpviewer_keywords:
- nop instruction
- __nop intrinsic
ms.assetid: 7a2a938b-87e0-476d-a348-03ea7635b6b9
ms.openlocfilehash: b0033b0e3a62a16c2856b0e25daeebdb5df0c81f
ms.sourcegitcommit: a1fad0a266b20b313364a74b16c9ac45d089b1e9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54220389"
---
# <a name="nop"></a>__nop

**Microsoft 전용**

아무 작업도 수행 하는 플랫폼별 기계어 코드를 생성 합니다.

## <a name="syntax"></a>구문

```
void __nop();
```

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__nop`|x86, ARM, x64, ARM64|

**헤더 파일** \<intrin.h >

**Microsoft 전용 종료**

## <a name="remarks"></a>설명

`__nop` 함수는 `NOP` 컴퓨터 명령에 해당합니다. X86 및 x64에 대 한 자세한 내용은 문서에 대해 검색 "Intel 아키텍처 소프트웨어 개발자 설명서 볼륨 2: 명령 집합 참조를 "에 [Intel Corporation](https://software.intel.com/articles/intel-sdm) 사이트입니다.

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[__noop](../intrinsics/noop.md)
