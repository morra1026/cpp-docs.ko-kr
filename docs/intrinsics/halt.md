---
title: __halt | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __halt
- __halt_cpp
dev_langs:
- C++
helpviewer_keywords:
- __halt intrinsic
- HLT instruction
ms.assetid: a074f44a-101c-45a5-8a5e-cfd223c34002
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a42575b25040b0dc78bd0199089aaf9575e8de47
ms.sourcegitcommit: a738519aa491a493a8f213971354356c0e6a5f3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/05/2018
ms.locfileid: "48820630"
---
# <a name="halt"></a>__halt

**Microsoft 전용**

설정 된 인터럽트, 마스크 불가능 인터럽트 (NMI) 또는 다시 설정 하는 발생 될 때까지 마이크로프로세서를 중단 합니다.

## <a name="syntax"></a>구문

```
void __halt( void );
```

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__halt`|x86, x64|

**헤더 파일** \<intrin.h >

## <a name="remarks"></a>설명

합니다 `__halt` 함수는 동일 합니다 `HLT` 컴퓨터 명령 및 커널 모드 에서만 사용할 수 있습니다. 자세한 내용은 문서를 검색 "Intel 아키텍처 소프트웨어 개발자 설명서 볼륨 2: 명령 집합 참조"에 [Intel Corporation](https://software.intel.com/articles/intel-sdm) 사이트입니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)