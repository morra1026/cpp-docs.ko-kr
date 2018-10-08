---
title: __nop | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __nop
dev_langs:
- C++
helpviewer_keywords:
- nop instruction
- __nop intrinsic
ms.assetid: 7a2a938b-87e0-476d-a348-03ea7635b6b9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bc5dab4ba2c23f60eb4407548cea5c15106c1401
ms.sourcegitcommit: a738519aa491a493a8f213971354356c0e6a5f3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/05/2018
ms.locfileid: "48820505"
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
|`__nop`|x86, x64|

**헤더 파일** \<intrin.h >

**Microsoft 전용 종료**

## <a name="remarks"></a>설명

합니다 `__nop` 함수는 동일 합니다 `NOP` 컴퓨터 명령입니다. 자세한 내용은 문서를 검색 "Intel 아키텍처 소프트웨어 개발자 설명서 볼륨 2: 명령 집합 참조"에 [Intel Corporation](https://software.intel.com/articles/intel-sdm) 사이트입니다.

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[__noop](../intrinsics/noop.md)