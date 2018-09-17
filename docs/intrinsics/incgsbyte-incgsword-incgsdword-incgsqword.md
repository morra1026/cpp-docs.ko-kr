---
title: __incgsbyte, __incgsword, __incgsdword, __incgsqword | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __incgsdword
- __incgsqword_cpp
- __incgsword_cpp
- __incgsword
- __incgsbyte
- __incgsbyte_cpp
- __incgsqword
- __incgsdword_cpp
dev_langs:
- C++
helpviewer_keywords:
- __incgsbyte intrinsic
- __incgsword intrinsic
- __incgsqword intrinsic
- __incgsdword intrinsic
ms.assetid: 06bfdf4f-7643-4fe0-8455-60ce3068073e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 611786246df9da54d94e673da1a5e48940ca7241
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45711128"
---
# <a name="incgsbyte-incgsword-incgsdword-incgsqword"></a>__incgsbyte, __incgsword, __incgsdword, __incgsqword
**Microsoft 전용**  
  
 값의 시작을 기준으로 오프셋으로 지정 된 메모리 위치에 추가 된 `GS` 세그먼트입니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __incgsbyte(   
   unsigned long Offset   
);  
void __incgsword(   
   unsigned long Offset   
);  
void __incgsdword(   
   unsigned long Offset  
);  
void __incgsqword(   
   unsigned long Offset   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
*오프셋*<br/>
[in] 시작 부분 으로부터의 오프셋 `GS`합니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__incgsbyte`|X64|  
|`__incgsword`|X64|  
|`__incgsdword`|X64|  
|`__incgsqword`|X64|  
  
## <a name="remarks"></a>설명  
 이러한 내장 함수 에서만 커널 모드에서 사용할 수 있으며 루틴은 내장 함수로 사용할 수 있습니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [__addgsbyte, \__addgsword, \__addgsdword, \__addgsqword](../intrinsics/addgsbyte-addgsword-addgsdword-addgsqword.md)   
 [__readgsbyte, \__readgsdword, \__readgsqword, \__readgsword](../intrinsics/readgsbyte-readgsdword-readgsqword-readgsword.md)   
 [__writegsbyte, \__writegsdword, \__writegsqword, \__writegsword](../intrinsics/writegsbyte-writegsdword-writegsqword-writegsword.md)   
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)