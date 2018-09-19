---
title: __writedr | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __writedr
dev_langs:
- C++
helpviewer_keywords:
- __writedr intrinsic
ms.assetid: ac55c1ee-df2f-41d4-a429-6f369d2a934d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b559edf26c847404d718440e86037cab4026297b
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45704953"
---
# <a name="writedr"></a>__writedr
지정 된 디버그 레지스터를 지정된 된 값을 씁니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __writedr(unsigned DebugRegister, unsigned DebugValue);  
void __writedr(unsigned DebugRegister, unsigned __int64 DebugValue);  
```  
  
#### <a name="parameters"></a>매개 변수  
*DebugRegister*<br/>
[in] 디버그를 식별 하는 0부터 7 까지의 숫자를 등록 합니다.  
  
*DebugValue*<br/>
[in] 디버그에 쓸 값을 등록 합니다.  
  
## <a name="remarks"></a>설명  
 이러한 내장 함수는 커널 모드 에서만 사용할 수 있습니다 및 루틴은 내장 함수로 사용할 수 있습니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__writedr`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__readdr](../intrinsics/readdr.md)