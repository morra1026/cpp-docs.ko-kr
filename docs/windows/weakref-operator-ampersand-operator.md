---
title: WeakRef::operator&amp; 연산자 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::WeakRef::operator&
dev_langs:
- C++
helpviewer_keywords:
- operator& operator
ms.assetid: 900afb73-3801-4d08-9b41-2e6a62011ccd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f8bb81ca1591fc398b1d0814fca918309169e82c
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42600986"
---
# <a name="weakrefoperatoramp-operator"></a>WeakRef::operator&amp; 연산자

반환 된 `ComPtrRef` 현재를 나타내는 개체 **WeakRef** 개체입니다.

## <a name="syntax"></a>구문

```cpp
Details::ComPtrRef<WeakRef> operator&() throw()  
```

## <a name="return-value"></a>반환 값

A `ComPtrRef` 현재 나타내는 **WeakRef** 개체입니다.

## <a name="remarks"></a>설명

코드에서 사용할 고려 하지 않은 한 내부 도우미 연산자입니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[WeakRef 클래스](../windows/weakref-class.md)