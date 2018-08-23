---
title: __addgsbyte, __addgsword, __addgsdword, __addgsqword | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __addgsdword
- __addgsqword
- __addgsword_cpp
- __addgsword
- __addgsbyte_cpp
- __addgsqword_cpp
- __addgsbyte
- __addgsdword_cpp
dev_langs:
- C++
helpviewer_keywords:
- __addgsword intrinsic
- __addgsqword intrinsic
- __addgsdword intrinsic
- __addgsbyte intrinsic
ms.assetid: 4fa03e69-d849-49ed-ba37-1d3aa23c2a21
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 50c0025e561c86fc18bbf5c4554c9f894fe32ec7
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42541301"
---
# <a name="addgsbyte-addgsword-addgsdword-addgsqword"></a>__addgsbyte, __addgsword, __addgsdword, __addgsqword
**Microsoft 전용**  
  
 값의 시작을 기준으로 오프셋으로 지정 된 메모리 위치에 추가 된 `GS` 세그먼트입니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __addgsbyte(   
   unsigned long Offset,   
   unsigned char Data   
);  
void __addgsword(   
   unsigned long Offset,   
   unsigned short Data   
);  
void __addgsdword(   
   unsigned long Offset,   
   unsigned long Data   
);  
void __addgsqword(   
   unsigned long Offset,   
   unsigned __int64 Data   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in] `Offset`  
 시작 부분 으로부터의 오프셋 `GS`합니다.  
  
 [in] `Data`  
 메모리 위치에 추가할 값입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__addgsbyte`|X64|  
|`__addgsword`|X64|  
|`__addgsdword`|X64|  
|`__addgsqword`|X64|  
  
## <a name="remarks"></a>설명  
 이러한 내장 함수는 커널 모드 에서만 사용할 수 있습니다 하 고 이러한 루틴은 내장 함수로 사용할 수 있습니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [__incgsbyte, \__incgsword, \__incgsdword, \__incgsqword](../intrinsics/incgsbyte-incgsword-incgsdword-incgsqword.md)   
 [__readgsbyte, \__readgsdword, \__readgsqword, \__readgsword](../intrinsics/readgsbyte-readgsdword-readgsqword-readgsword.md)   
 [__writegsbyte, \__writegsdword, \__writegsqword, \__writegsword](../intrinsics/writegsbyte-writegsdword-writegsqword-writegsword.md)   
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)