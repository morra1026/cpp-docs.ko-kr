---
title: raw_method_prefix | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- raw_method_prefix
dev_langs:
- C++
helpviewer_keywords:
- raw_method_prefix attribute
ms.assetid: 71490313-af78-4bb2-b28a-eee67950d30b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fc2a37f587d3b5ac2b695171f5620db6521693d2
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46439681"
---
# <a name="rawmethodprefix"></a>raw_method_prefix
**C + + 전용**  
  
이름 충돌을 방지하기 위해 다른 접두사를 지정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
raw_method_prefix("Prefix")  
```  
  
### <a name="parameters"></a>매개 변수  
*접두사*  
사용할 접두사입니다.  
  
## <a name="remarks"></a>설명  
 
하위 수준 속성 및 메서드는 기본 접두사를 사용 하 여 명명 된 멤버 함수에 의해 노출 되 **raw_** 고급 오류 처리 멤버 함수를 사용 하 여 이름 충돌을 방지 합니다.  
  
> [!NOTE]
> 효과 **raw_method_prefix** 특성으로 변경 되지 것입니다 합니다 [raw_interfaces_only](#_predir_raw_interfaces_only) 특성입니다. 합니다 **raw_method_prefix** 항상 우선 `raw_interfaces_only` 접두사를 지정 합니다. 동일한 특성을 모두 사용 하는 경우 `#import` 문 다음에 지정 된 접두사가 합니다 **raw_method_prefix** 특성을 사용 합니다.  
  
**C + + 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 
[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)