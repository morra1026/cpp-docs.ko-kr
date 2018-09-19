---
title: __vmx_vmread | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __vmx_vmread
dev_langs:
- C++
helpviewer_keywords:
- VMREAD instruction
- __vmx_vmread intrinsic
ms.assetid: 08bdd7a0-6435-4ea6-b9a0-f592d870e5aa
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c0c8b5a22cfef8ebde74fbe6d1f6920a969e7bc6
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706383"
---
# <a name="vmxvmread"></a>__vmx_vmread
**Microsoft 전용**  
  
 현재 가상 머신 제어 구조 (VMCS)에 지정된 된 필드를 읽고 지정된 된 위치에 배치 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned char __vmx_vmread(  
   size_t Field,  
   size_t *FieldValue  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|*필드*|[in] VMCS의 필드는 읽기입니다.|  
|*FieldValue*|[in] 지정 하 여 VMCS 필드에서 읽은 값을 저장할 위치에 대 한 포인터를 `Field` 매개 변수입니다.|  
  
## <a name="return-value"></a>반환 값  
  
|값|의미|  
|-----------|-------------|  
|0|작업에 성공했습니다.|  
|1|현재 VMCS의 `VM-instruction error field` 에서 사용할 수 있는 확장된 상태로 작업이 실패했습니다.|  
|2|사용 가능한 상태 없이 작업이 실패했습니다.|  
  
## <a name="remarks"></a>설명  
 합니다 `__vmx_vmread` 함수는 동일 합니다 `VMREAD` 컴퓨터 명령입니다. 값을 `Field` 매개 변수는 Intel 설명서에 설명 된 인코딩된 필드 인덱스입니다. 자세한 내용은 "Intel 가상화 기술 사양에 대 한는 IA-32 Intel 아키텍처" 문서를 검색에서 숫자 C97063-002, 문서를 [Intel Corporation](https://software.intel.com/en-us/articles/intel-sdm) 사이트를 다음 문서의 부록 C를 참조 하세요. .  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__vmx_vmread`|X64|  
  
 **헤더 파일** \<intrin.h >  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__vmx_vmwrite](../intrinsics/vmx-vmwrite.md)