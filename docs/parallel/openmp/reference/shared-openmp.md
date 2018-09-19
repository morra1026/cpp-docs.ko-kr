---
title: 공유 (OpenMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- Shared
dev_langs:
- C++
helpviewer_keywords:
- shared OpenMP clause
ms.assetid: 7887dc95-67a2-462f-a3a2-8e0632bf5d04
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 078d4b01d2c797fa11c3603c79a341f75e11f18c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46115478"
---
# <a name="shared-openmp"></a>shared (OpenMP)
하나 이상의 변수는 모든 스레드 간에 공유 해야 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
shared(var)  
```  
  
### <a name="parameters"></a>매개 변수
  
*var*<br/>
하나 이상의 변수를 공유 합니다. 둘 이상의 변수를 지정할 경우 쉼표를 사용 하 여 변수 이름을 구분 합니다.  
  
## <a name="remarks"></a>설명  
 스레드 간에 변수를 공유 하는 또 다른 방법은 된 합니다 [copyprivate](../../../parallel/openmp/reference/copyprivate.md) 절.  
  
 `shared` 다음 지시문에 적용 됩니다.  
  
-   [for](../../../parallel/openmp/reference/for-openmp.md)  
  
-   [parallel](../../../parallel/openmp/reference/parallel.md)  
  
-   [섹션](../../../parallel/openmp/reference/sections-openmp.md)  
  
 자세한 내용은 [2.7.2.4 공유](../../../parallel/openmp/2-7-2-4-shared.md)합니다.  
  
## <a name="example"></a>예제  
 참조 [사설](../../../parallel/openmp/reference/private-openmp.md) 사용 하는 예제에 대 한 `shared`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [절](../../../parallel/openmp/reference/openmp-clauses.md)