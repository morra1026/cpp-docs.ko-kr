---
title: __lidt | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __lidt
- __lidt_cpp
dev_langs:
- C++
helpviewer_keywords:
- LIDT instruction
- __lidt intrinsic
ms.assetid: 8298d25d-a19e-4900-828d-6b3b09841882
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5184d925e5d6712dd547e34341d84919c50e0a43
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45724713"
---
# <a name="lidt"></a>__lidt
**Microsoft 전용**  
  
 지정된 된 메모리 위치에 있는 값을 사용 하 여 인터럽트 설명자 테이블 레지스터 (IDTR)를 로드합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __lidt(  
     void *Source);  
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|*Source*|[in] IDTR 복사할 값에 대 한 포인터입니다.|  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__lidt`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
## <a name="remarks"></a>설명  
 합니다 `__lidt` 함수는 동일 합니다 `LIDT` 컴퓨터 명령 및 커널 모드 에서만 사용할 수 있습니다. 자세한 내용은 문서를 검색 "Intel 아키텍처 소프트웨어 개발자 설명서 볼륨 2: 명령 집합 참조"에 [Intel Corporation](https://software.intel.com/en-us/articles/intel-sdm) 사이트입니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__sidt](../intrinsics/sidt.md)