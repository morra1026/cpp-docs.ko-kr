---
title: 'Argtraits:: Args 상수 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::ArgTraits::args
dev_langs:
- C++
helpviewer_keywords:
- args constant
ms.assetid: a68100ab-254b-4571-a0bc-946f1633a46b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 0600f3a6f220d54085ff7c2ff8d60c2148ced625
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42593312"
---
# <a name="argtraitsargs-constant"></a>ArgTraits::args 상수

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
static const int args = -1; ;
```

## <a name="remarks"></a>설명

매개 변수 개수를 유지 합니다 `Invoke` 대리자 인터페이스의 메서드입니다.

## <a name="remarks"></a>설명

때 **args** 가-1에 일치 수를 나타냅니다는 `Invoke` 메서드 시그니처입니다.

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[ArgTraits 구조체](../windows/argtraits-structure.md)  
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)