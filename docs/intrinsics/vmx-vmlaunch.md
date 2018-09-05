---
title: __vmx_vmlaunch | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __vmx_vmlaunch
dev_langs:
- C++
helpviewer_keywords:
- VMLAUNCH instruction
- __vmx_vmlaunch intrinsic
ms.assetid: 708f7c38-b7c1-4ee7-bfc4-0daeb9cc9360
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9a0d7b5b26c5cf805e0fef8c5fb2785ebf3712b4
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43678479"
---
# <a name="vmxvmlaunch"></a>__vmx_vmlaunch
**Microsoft 전용**  
  
 현재 가상 머신 제어 구조 (VMCS)를 사용 하 여 VMX 루트가 아닌 작업 상태 (VM 입력)에서 호출 응용 프로그램을 배치 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned char __vmx_vmlaunch(  
   void);  
```  
  
## <a name="return-value"></a>반환 값  
  
|값|의미|  
|-----------|-------------|  
|0|작업에 성공했습니다.|  
|1|현재 VMCS의 `VM-instruction error field` 에서 사용할 수 있는 확장된 상태로 작업이 실패했습니다.|  
|2|사용 가능한 상태 없이 작업이 실패했습니다.|  
  
## <a name="remarks"></a>설명  
 응용 프로그램이 사용 하 여 VM 시작 작업을 수행할 수는 [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) 하거나 [__vmx_vmresume](../intrinsics/vmx-vmresume.md) 함수입니다. 합니다 [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) 함수는 시작 상태가 인 vmcs 에서만 사용할 수 있습니다 `Clear`, 및 [__vmx_vmresume](../intrinsics/vmx-vmresume.md) 함수는 시작 상태가 인 vmcs 에서만 사용할 수 있습니다 `Launched`합니다. 따라서 사용 하 여는 [__vmx_vmclear](../intrinsics/vmx-vmclear.md) 에 VMCS의 시작 상태를 설정 하는 함수 `Clear`를 사용 하 여를 [__vmx_vmlaunch](../intrinsics/vmx-vmlaunch.md) 함수에 첫 번째 VM 시작 작업에는 [__vmx_vmresume](../intrinsics/vmx-vmresume.md) 이후 VM 시작 작업에 대 한 함수입니다.  
  
 합니다 `__vmx_vmlaunch` 함수는 동일 합니다 `VMLAUNCH` 컴퓨터 명령입니다. 이 함수는 게스트 운영 체제 및 해당 응용 프로그램과 호스트 가상 머신 모니터의 상호 작용을 지원합니다. 자세한 내용은 "Intel 가상화 기술 사양에 대 한는 IA-32 Intel 아키텍처" 문서를 검색에서 숫자 C97063-002를 문서화 합니다 [Intel Corporation](https://software.intel.com/en-us/articles/intel-sdm) 사이트입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__vmx_vmlaunch`|X64|  
  
 **헤더 파일** \<intrin.h >  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__vmx_vmresume](../intrinsics/vmx-vmresume.md)   
 [__vmx_vmclear](../intrinsics/vmx-vmclear.md)