---
title: __vmx_vmptrld | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __vmx_vmptrld
dev_langs:
- C++
helpviewer_keywords:
- __vmx_vmptrld intrinsic
- VMPTRLD instruction
ms.assetid: 95c9ec5b-1a81-41ba-983e-327bd6a65fcb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4f3304106662d290a208545061bf9f71b7f30c10
ms.sourcegitcommit: a738519aa491a493a8f213971354356c0e6a5f3a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/05/2018
ms.locfileid: "48820947"
---
# <a name="vmxvmptrld"></a>__vmx_vmptrld

**Microsoft 전용**

지정된 된 주소에서 현재 가상 머신 제어 구조 (VMCS)에 대 한 포인터를 로드합니다.

## <a name="syntax"></a>구문

```
int __vmx_vmptrld( 
   unsigned __int64 *VmcsPhysicalAddress 
);
```

#### <a name="parameters"></a>매개 변수

[in] *`VmcsPhysicalAddress` VMCS 포인터 저장 되는 주소입니다.

## <a name="return-value"></a>반환 값

작업이 성공적으로 수행 하는 0입니다.

1에서 사용할 수 있는 확장 된 상태를 사용 하 여 작업이 실패 합니다 `VM-instruction error field` 현재 VMCS의 합니다.

2 사용 가능한 상태 없이 작업에 실패 했습니다.

## <a name="remarks"></a>설명

VMCS 포인터는 64 비트 물리적 주소입니다.

합니다 `__vmx_vmptrld` 함수는 동일 합니다 `VMPTRLD` 컴퓨터 명령입니다. 이 함수는 게스트 운영 체제 및 해당 응용 프로그램과 호스트 가상 머신 모니터의 상호 작용을 지원합니다. 자세한 내용은 "Intel 가상화 기술 사양에 대 한는 IA-32 Intel 아키텍처" 문서를 검색에서 숫자 C97063-002를 문서화 합니다 [Intel Corporation](https://software.intel.com/articles/intel-sdm) 사이트입니다.

## <a name="requirements"></a>요구 사항

|내장 함수|아키텍처|
|---------------|------------------|
|`__vmx_vmptrld`|X64|

**헤더 파일** \<intrin.h >

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)<br/>
[__vmx_vmptrst](../intrinsics/vmx-vmptrst.md)