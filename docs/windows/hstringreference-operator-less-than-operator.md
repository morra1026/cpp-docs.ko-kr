---
title: 'Hstringreference:: Operator&lt; 연산자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HStringReference::operator<
dev_langs:
- C++
ms.assetid: 55aa48e8-7c96-4123-9ebe-42b4cd8b9377
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ee7edbee285df6da752e875ac4d86a74e8f7893d
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42594143"
---
# <a name="hstringreferenceoperatorlt-operator"></a>Hstringreference:: Operator&lt; 연산자

첫 번째 매개 변수 인지 보다 작은 두 번째 매개 변수를 나타냅니다.

## <a name="syntax"></a>구문

```cpp
inline bool operator<(
    const HStringReference& lhs,
    const HStringReference& rhs) throw()  
```

### <a name="parameters"></a>매개 변수

*lhs*  
비교할 첫 번째 매개 변수입니다. *lhs* 에 대 한 참조 수를 **HStringReference**합니다.

*rhs*  
비교할 두 번째 매개 변수입니다.  *rhs* 에 대 한 참조 수를 **HStringReference**합니다.

## <a name="return-value"></a>반환 값

**true** 경우는 *lhs* 매개 변수는 보다 작은 *rhs* 매개 변수가 고, 그렇지 않으면 **false**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HStringReference 클래스](../windows/hstringreference-class.md)