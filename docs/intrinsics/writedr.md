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
ms.openlocfilehash: 598b95df8fd2f4dd2826fcfa1f59a7e2daa8d523
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42545888"
---
# <a name="writedr"></a>__writedr
지정 된 디버그 레지스터를 지정된 된 값을 씁니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __writedr(unsigned DebugRegister, unsigned DebugValue);  
void __writedr(unsigned DebugRegister, unsigned __int64 DebugValue);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in] `DebugRegister`  
 디버그를 식별 하는 0부터 7 까지의 숫자를 등록 합니다.  
  
 [in] `DebugValue`  
 디버그에 쓸 값을 등록 합니다.  
  
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