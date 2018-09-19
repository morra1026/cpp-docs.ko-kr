---
title: lastprivate | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- lastprivate
dev_langs:
- C++
helpviewer_keywords:
- lastprivate OpenMP clause
ms.assetid: 6ef87b31-375a-47e8-8d0d-281be45fb56a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c87dfc47f7f2554e75567a1de4ea9cb2e06eaa00
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46028196"
---
# <a name="lastprivate"></a>lastprivate
변수는 바깥쪽 컨텍스트에서 버전 어떤 스레드가 실행 마지막 반복 (루프에 대 한 구성) 또는 마지막 섹션 (#pragma 섹션)의 개인 버전 설정 되어 있는지를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
lastprivate(var)  
```  
  
### <a name="parameters"></a>매개 변수
  
*var*<br/>
어떤 스레드의 개인 버전으로 설정 하는 변수는 마지막 반복 (루프에 대 한 구성) 또는 마지막 섹션 (#pragma 섹션)을 실행 합니다.  
  
## <a name="remarks"></a>설명  
 `lastprivate` 다음 지시문에 적용 됩니다.  
  
-   [for](../../../parallel/openmp/reference/for-openmp.md)  
  
-   [섹션](../../../parallel/openmp/reference/sections-openmp.md)  
  
 자세한 내용은 [2.7.2.3 lastprivate](../../../parallel/openmp/2-7-2-3-lastprivate.md)합니다.  
  
## <a name="example"></a>예제  
 참조 [일정](../../../parallel/openmp/reference/schedule.md) 사용 하는 예제에 대 한 `lastprivate` 절.  
  
## <a name="see-also"></a>참고 항목  
 [절](../../../parallel/openmp/reference/openmp-clauses.md)