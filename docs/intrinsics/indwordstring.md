---
title: __indwordstring | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __indwordstring
- __indwordstring_cpp
dev_langs:
- C++
helpviewer_keywords:
- __indwordstring intrinsic
- rep insd instruction
ms.assetid: 96a1cf33-f691-4916-99e4-fa849b61e3a9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2c504b4f9a17c65affbcc2635ef63ec743f7ad93
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45700897"
---
# <a name="indwordstring"></a>__indwordstring
**Microsoft 전용**  
  
 사용 하 여 지정 된 포트에서 데이터를 읽고는 `rep insd` 명령입니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __indwordstring(  
   unsigned short Port,  
   unsigned long* Buffer,  
   unsigned long Count  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
*포트*<br/>
[in] 포트에서 읽기입니다.  
  
*Buffer*<br/>
[out] 여기에 포트에서 읽은 데이터가 기록 됩니다.  
  
*개수*<br/>
[in] 읽을 데이터의 바이트 수입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__indwordstring`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
## <a name="remarks"></a>설명  
 이 루틴은 내장 루틴으로만 사용할 수 있습니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)