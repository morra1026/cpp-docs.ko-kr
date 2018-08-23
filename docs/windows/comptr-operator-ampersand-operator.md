---
title: 'Comptr:: Operator&amp; 연산자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::ComPtr::operator&
dev_langs:
- C++
helpviewer_keywords:
- operator& operator
ms.assetid: 2d77fda6-f4b2-45c1-8a0e-fbc355013531
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f513ac83e0ee83109f42cf87b80b4fcc4960db1f
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42598605"
---
# <a name="comptroperatoramp-operator"></a>Comptr:: Operator&amp; 연산자

와 연결 된 인터페이스를 해제 **ComPtr** 개체를 다음의 주소를 검색 합니다 **ComPtr** 개체입니다.

## <a name="syntax"></a>구문

```cpp
Details::ComPtrRef<WeakRef> operator&()

const Details::ComPtrRef<const WeakRef> operator&() const
```

## <a name="return-value"></a>반환 값

약한 참조를 현재 **ComPtr**합니다.

## <a name="remarks"></a>설명

이 방법은에서 다릅니다 [comptr:: Getaddressof](../windows/comptr-getaddressof-method.md) 는이 메서드는 인터페이스 포인터에 대 한 참조를 해제 합니다. 사용 하 여 `ComPtr::GetAddressOf` 인터페이스 포인터의 주소가 필요 하지만 해당 인터페이스를 해제 하지 않으려는 경우.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[ComPtr 클래스](../windows/comptr-class.md)