---
title: 'Weakref:: Weakref 생성자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::WeakRef::WeakRef
dev_langs:
- C++
helpviewer_keywords:
- WeakRef, constructor
ms.assetid: 589f87e0-8dcc-4e82-aab2-f2f66f1ec47c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d7c8bc81040ce8d4c1cea7497f9d1371fbb9d41f
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42611612"
---
# <a name="weakrefweakref-constructor"></a>WeakRef::WeakRef 생성자

새 인스턴스를 초기화 합니다 **WeakRef** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
WeakRef();
WeakRef(
   decltype(__nullptr)  
);

WeakRef(
   _In_opt_ IWeakReference* ptr
);

WeakRef(
   const ComPtr<IWeakReference>& ptr
);

WeakRef(
   const WeakRef& ptr
);

WeakRef(
   _Inout_ WeakRef&& ptr
);
```

### <a name="parameters"></a>매개 변수

*ptr*  
포인터, 참조 또는 현재 초기화 하는 기존 개체에 대 한 rvalue 참조 **WeakRef** 개체입니다.

## <a name="remarks"></a>설명

첫 번째 생성자는 빈 **WeakRef** 개체입니다. 두 번째 생성자는 초기화를 **WeakRef** 개체에 대 한 포인터를 `IWeakReference` 인터페이스입니다. 세 번째 생성자는 초기화를 **WeakRef** 개체에 대 한 참조를 `ComPtr<IWeakReference>` 개체입니다. 네 번째와 다섯 번째 생성자 초기화를 **WeakRef** 개체를 서로 **WeakRef** 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[WeakRef 클래스](../windows/weakref-class.md)