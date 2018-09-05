---
title: __vmx_vmwrite | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __vmx_vmwrite
dev_langs:
- C++
helpviewer_keywords:
- __vmx_vmwrite intrinsic
- VMWRITE instruction
ms.assetid: 88139792-fd3f-4210-97ca-9d84f43a0252
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 132841c8c24e2b625dad218aaaef2a19cba0a264
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43680500"
---
# <a name="vmxvmwrite"></a>__vmx_vmwrite
**Microsoft 전용**  
  
 현재 가상 머신 제어 구조 (VMCS)에 지정된 된 필드를 지정된 된 값을 씁니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned char __vmx_vmwrite(   
   size_t Field,  
   size_t FieldValue  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|[in] `Field`|쓸 VMCS 필드입니다.|  
|[in] `FieldValue`|VMCS 필드에 쓸 값입니다.|  
  
## <a name="return-value"></a>반환 값  
 0  
 작업에 성공했습니다.  
  
 1  
 현재 VMCS의 `VM-instruction error field` 에서 사용할 수 있는 확장된 상태로 작업이 실패했습니다.  
  
 2  
 사용 가능한 상태 없이 작업이 실패했습니다.  
  
## <a name="remarks"></a>설명  
 합니다 `__vmx_vmwrite` 함수는 동일 합니다 `VMWRITE` 컴퓨터 명령입니다. 값을 `Field` 매개 변수는 Intel 설명서에 설명 된 인코딩된 필드 인덱스입니다. 자세한 내용은 "Intel 가상화 기술 사양에 대 한는 IA-32 Intel 아키텍처" 문서를 검색에서 숫자 C97063-002, 문서를 [Intel Corporation](https://software.intel.com/en-us/articles/intel-sdm) 사이트 및 다음의 부록 C를 참조 하세요. 문서입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__vmx_vmwrite`|X64|  
  
 **헤더 파일** \<intrin.h >  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__vmx_vmread](../intrinsics/vmx-vmread.md)