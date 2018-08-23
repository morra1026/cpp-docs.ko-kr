---
title: __indword | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __indword_cpp
- __indword
dev_langs:
- C++
helpviewer_keywords:
- in instruction
- __indword intrinsic
ms.assetid: 1068d686-586e-4e36-b962-d1d7c3315260
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c0fb7c8d6816475232f5a7ed5d50b2b6036a829d
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42545873"
---
# <a name="indword"></a>__indword
**Microsoft 전용**  
  
 데이터의 2 배 워드를 하나 사용 하 여 지정 된 포트에서 읽기를 `in` 명령입니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned long __indword(  
   unsigned short Port  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in] `Port`  
 포트에서 읽기입니다.  
  
## <a name="return-value"></a>반환 값  
 단어 포트에서 읽습니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__indword`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
## <a name="remarks"></a>설명  
 이 루틴은 내장 루틴으로만 사용할 수 있습니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)