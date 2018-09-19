---
title: __writegsbyte, __writegsdword, __writegsqword, __writegsword | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __writegsbyte
- __writegsqword
- __writegsdword
- __writegsword
dev_langs:
- C++
helpviewer_keywords:
- __writegsqword intrinsic
- __writegsbyte intrinsic
- __writegsword intrinsic
- __writegsdword intrinsic
ms.assetid: 7746cf6d-2259-4139-9aab-c07dd75c8037
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8376300f4234f355cce49c2aae90fdc0e67f9a18
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725870"
---
# <a name="writegsbyte-writegsdword-writegsqword-writegsword"></a>__writegsbyte, __writegsdword, __writegsqword, __writegsword
**Microsoft 전용**  
  
 GS 세그먼트의 시작을 기준으로 오프셋으로 지정 된 위치에 메모리를 작성 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void __writegsbyte(   
   unsigned long Offset,   
   unsigned char Data   
);  
void __writegsword(   
   unsigned long Offset,   
   unsigned short Data   
);  
void __writegsdword(   
   unsigned long Offset,   
   unsigned long Data   
);  
void __writegsqword(   
   unsigned long Offset,   
   unsigned __int64 Data   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
*오프셋*<br/>
[in] 쓸 GS 시작 부분 으로부터의 오프셋입니다.  
  
*Data*<br/>
[in] 쓸 값입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`__writegsbyte`|X64|  
|`__writegsdword`|X64|  
|`__writegsqword`|X64|  
|`__writegsword`|X64|  
  
 **헤더 파일** \<intrin.h >  
  
## <a name="remarks"></a>설명  
 이러한 내장 함수는 커널 모드 에서만 사용할 수 있습니다 하 고 이러한 루틴은 내장 함수로 사용할 수 있습니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [__readgsbyte, \__readgsdword, \__readgsqword, \__readgsword](../intrinsics/readgsbyte-readgsdword-readgsqword-readgsword.md)   
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)