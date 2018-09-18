---
title: copyin | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- copyin
dev_langs:
- C++
helpviewer_keywords:
- copyin OpenMP clause
ms.assetid: 369efa88-613c-4cb1-9e11-7b9ee08a4b25
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 27afaee16a87ddf428570f7854212eed34634d38
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46059331"
---
# <a name="copyin"></a>copyin
스레드가 마스터 스레드에 값에 대 한 액세스 하도록 허용 된 [threadprivate](../../../parallel/openmp/reference/threadprivate.md) 변수입니다.  
  
## <a name="syntax"></a>구문  
  
```  
copyin(var)  
```  
  
## <a name="parameters"></a>매개 변수
  
*var*<br/>
`threadprivate` 변수는 병렬 구문 전에 있으므로 마스터 스레드에서 변수의 값으로 초기화 됩니다.  
  
## <a name="remarks"></a>설명  
 `copyin` 다음 지시문에 적용 됩니다.  
  
-   [parallel](../../../parallel/openmp/reference/parallel.md)  
  
-   [for](../../../parallel/openmp/reference/for-openmp.md)  
  
-   [섹션](../../../parallel/openmp/reference/sections-openmp.md)  
  
 자세한 내용은 [2.7.2.7 copyin](../../../parallel/openmp/2-7-2-7-copyin.md)합니다.  
  
## <a name="example"></a>예제  
 참조 [threadprivate](../../../parallel/openmp/reference/threadprivate.md) 사용 하는 예제에 대 한 `copyin`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [절](../../../parallel/openmp/reference/openmp-clauses.md)