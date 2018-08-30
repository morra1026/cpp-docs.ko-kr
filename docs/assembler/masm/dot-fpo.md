---
title: . FPO | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- .FPO
dev_langs:
- C++
helpviewer_keywords:
- .FPO directive
ms.assetid: 35f4cd61-32f9-4262-b657-73f04f775d09
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 234ec5bd703a390d1e2ee60e48d99d346d4aad95
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43203115"
---
# <a name="fpo"></a>.FPO
합니다. FPO 지시문 디버그 레코드를.debug$ F 세그먼트 또는 섹션의 내보내기가 제어합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
FPO (  
cdwLocals  
,   
cdwParams  
,   
cbProlog  
,   
cbRegs  
,   
fUseBP  
,   
cbFrame  
)  
  
```  
  
#### <a name="parameters"></a>매개 변수  
 `cdwLocals`  
 지역 변수는 부호 없는 32 비트 값의 수입니다.  
  
 `cdwParams`  
 DWORD, 부호 없는 16 비트 값을 매개 변수 크기입니다.  
  
 *cbProlog*  
 함수 프롤로그 코드에서 부호 없는 8 비트 값을 바이트 수입니다.  
  
 `cbRegs`  
 저장 된 레지스터 번호입니다.  
  
 `fUseBP`  
 EBP 레지스터에 할당 되어 있는지 여부를 나타냅니다. 0 또는 1입니다.  
  
 *cbFrame*  
 프레임 유형을 나타냅니다.  참조 [FPO_DATA](/windows/desktop/api/winnt/ns-winnt-_fpo_data) 자세한 내용은 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [지시문 참조](../../assembler/masm/directives-reference.md)