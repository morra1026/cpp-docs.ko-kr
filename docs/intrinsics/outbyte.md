---
title: __outbyte | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __outbyte
dev_langs:
- C++
helpviewer_keywords:
- out instruction
- __outbyte intrinsic
ms.assetid: c4cd1a34-8a02-4e37-993d-3201bc17901a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 70aa643d7d8f81cca0ff74a3016badd6551c11a0
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42538757"
---
# <a name="outbyte"></a>__outbyte
**Microsoft 전용**  
  
 생성 된 `out` 명령으로 지정 된 1 바이트를 전송 하는 `Data` 로 지정 된 I/O 포트를 찾기 `Port`합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __outbyte(   
   unsigned short Port,   
   unsigned char Data   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in] `Port`  
 데이터를 보낼 포트입니다.  
  
 [in] `Data`  
 지정된 된 포트에 보내도록 바이트입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__outbyte`|x86, x64|  
  
 **헤더 파일** \<intrin.h >  
  
## <a name="remarks"></a>설명  
 이 루틴은 내장 루틴으로만 사용할 수 있습니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)