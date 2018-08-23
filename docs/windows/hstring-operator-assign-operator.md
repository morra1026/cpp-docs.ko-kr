---
title: 'Hstring:: Operator = 연산자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HString::operator=
dev_langs:
- C++
ms.assetid: 8e68c1ff-bc57-4526-810e-af3c284b4e30
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9294650db7a1b18c2542603988952a80b3f1905d
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42598547"
---
# <a name="hstringoperator-operator"></a>HString::Operator= 연산자

다른 값으로 이동 **HString** 개체를 현재 **HString** 개체입니다.

## <a name="syntax"></a>구문

```cpp
HString& operator=(HString&& other) throw()  
```

### <a name="parameters"></a>매개 변수

*other*  
기존 **HString** 개체입니다.

## <a name="remarks"></a>설명

기존 값 *다른* 현재 개체를 복사할 **HString** 개체를 차례로 합니다 *다른* 개체는 소멸 됩니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HString 클래스](../windows/hstring-class.md)