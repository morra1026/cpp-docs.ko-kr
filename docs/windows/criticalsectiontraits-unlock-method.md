---
title: 'Criticalsectiontraits:: Unlock 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::CriticalSectionTraits::Unlock
dev_langs:
- C++
helpviewer_keywords:
- Unlock method
ms.assetid: 8fb382f5-6eda-407e-9673-71d77bda4962
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5babc5c14baae474409cd364af31b70549fcefe5
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413018"
---
# <a name="criticalsectiontraitsunlock-method"></a>CriticalSectionTraits::Unlock 메서드

특수화는 `CriticalSection` 를 지정 된 임계 영역 개체의 해제 소유권 지원 하므로 템플릿.

## <a name="syntax"></a>구문

```cpp
inline static void Unlock(
   _In_ Type cs
);
```

### <a name="parameters"></a>매개 변수

*cs*<br/>
임계 영역 개체에 대 한 포인터입니다.

## <a name="remarks"></a>설명

합니다 `Type` 한정자로 정의 된 `typedef CRITICAL_SECTION* Type;`합니다.

자세한 내용은 **LeaveCriticalSection 함수** 에 **동기화 함수** Windows API 설명서의 섹션입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="see-also"></a>참고 항목

[CriticalSectionTraits 구조체](../windows/criticalsectiontraits-structure.md)