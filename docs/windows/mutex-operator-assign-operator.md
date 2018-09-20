---
title: 'Mutex:: operator = 연산자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Mutex::operator=
dev_langs:
- C++
helpviewer_keywords:
- operator= operator
ms.assetid: 9b0ee206-a930-4fea-8dc0-1f79839e9d13
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ea5aee6f248487097462028a763a98b4e814a17a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46396794"
---
# <a name="mutexoperator-operator"></a>Mutex::operator= 연산자

할당 된 (이동) **뮤텍스** 개체를 현재 **뮤텍스** 개체입니다.

## <a name="syntax"></a>구문

```cpp
Mutex& operator=(
   _Inout_ Mutex&& h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
rvalue 참조를 **뮤텍스** 개체입니다.

## <a name="return-value"></a>반환 값

현재에 대 한 참조가 **뮤텍스** 개체입니다.

## <a name="remarks"></a>설명

자세한 내용은 참조는 **이동 의미 체계** 부분 [Rvalue 참조 선언 자: & &](../cpp/rvalue-reference-declarator-amp-amp.md)합니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[Mutex 클래스](../windows/mutex-class1.md)