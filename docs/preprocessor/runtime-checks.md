---
title: runtime_checks | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- vc-pragma.runtime_checks
- runtime_checks_CPP
dev_langs:
- C++
helpviewer_keywords:
- runtime_checks pragma
- pragmas, runtime_checks
ms.assetid: ae50b43f-f88d-47ad-a2db-3389e9e7df5b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b20ea9dd12bfe4daff8e2e440c96a41c220aa742
ms.sourcegitcommit: d4c803bd3a684d7951bf88dcecf1f14af43ae411
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/10/2018
ms.locfileid: "42540257"
---
# <a name="runtimechecks"></a>runtime_checks
[/RTC](../build/reference/rtc-run-time-error-checks.md) 설정을 사용할 수 없도록 설정하거나 복원합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#pragma runtime_checks( "[runtime_checks]", {restore | off} )  
```  
  
## <a name="remarks"></a>설명  
 
컴파일러 옵션으로 설정되지 않은 런타임 검사를 사용할 수 없습니다. 예를 들어, 지정 하지 않는 경우 `/RTCs`지정, `#pragma runtime_checks( "s", restore)` 가 스택 프레임 유효성 확인을 사용 하지 않습니다.  
  
**runtime_checks** pragma는 함수 외부에 있어야 하며 pragma가 표시된 후에 정의된 첫 번째 함수에 적용됩니다. *복원* 및 *해제* 인수에 지정 된 옵션을 설정 합니다 **runtime_checks** 또는 해제 합니다.  
  
합니다 **runtime_checks** 다음 표에 나와 있는 매개 변수를 0 개 이상의 될 수 있습니다.  
  
### <a name="parameters-of-the-runtimechecks-pragma"></a>runtime_checks Pragma의 매개 변수  
  
|매개 변수|런타임 검사 형식|  
|--------------------|-----------------------------|  
|*s*|스택(프레임)을 확인하도록 설정합니다.|  
|*c*|데이터 손실이 발생하는 더 작은 데이터 형식에 값이 할당되는 경우 이를 보고합니다.|  
|*u*|정의되기 전에 변수를 사용하면 보고합니다.|  
  
이 동일한 문자 사용을 `/RTC` 컴파일러 옵션입니다. 예를 들어:  
  
```  
#pragma runtime_checks( "sc", restore )  
```  
  
**runtime_checks** pragma를 빈 문자열(**""**)과 함께 사용하는 것은 특별한 형태의 지시문입니다.  
  
- 사용 하는 경우는 *해제* 매개 변수를 해제 위의 표에 나열 된 런타임 오류 검사를 설정 합니다.  
  
- 사용 하는 경우는 *복원* 매개 변수를 런타임 오류 검사를 재설정 지정 된 된 `/RTC` 컴파일러 옵션입니다.  
  
```  
#pragma runtime_checks( "", off )  
.  
.  
.  
#pragma runtime_checks( "", restore )   
```  
  
## <a name="see-also"></a>참고 항목  
 
[Pragma 지시문 및 __Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)   