---
title: __readeflags | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __readeflags
dev_langs:
- C++
helpviewer_keywords:
- __readeflags intrinsic
ms.assetid: f9d2f4d8-c428-491f-b8de-04d0566b2b6b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a6488cc42519bbbee8c8fefb242996144f6bb8a8
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42540705"
---
# <a name="readeflags"></a>__readeflags
등록 프로그램 상태 및 컨트롤 (EFLAGS)을 읽습니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned     int __readeflags(void);  
unsigned __int64 __readeflags(void);  
```  
  
## <a name="return-value"></a>반환 값  
 EFLAGS 레지스터의 값입니다. 반환 값은 32 비트 및 64 비트 long 32 비트 플랫폼에서 64 비트 플랫폼에서 긴 합니다.  
  
## <a name="remarks"></a>설명  
 이러한 루틴은 내장 함수로 사용할 수 있습니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__readeflags`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [__writeeflags](../intrinsics/writeeflags.md)