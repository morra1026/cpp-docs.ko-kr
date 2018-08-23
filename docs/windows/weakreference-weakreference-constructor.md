---
title: 'Weakreference:: Weakreference 생성자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::WeakReference::WeakReference
dev_langs:
- C++
helpviewer_keywords:
- WeakReference, constructor
ms.assetid: 4959a9d7-78ea-423d-a46b-50d010d29fff
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d506bc99d584222de55de56c9efbe40f9c71434a
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42593495"
---
# <a name="weakreferenceweakreference-constructor"></a>WeakReference::WeakReference 생성자

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
WeakReference();
```

## <a name="remarks"></a>설명

새 인스턴스를 초기화 합니다 [WeakReference 클래스](../windows/weakreference-class1.md)합니다.

에 대 한 강력한 참조 포인터를 **WeakReference** 개체에 초기화 됩니다 **nullptr**, 및 강력한 참조 횟수를 1로 초기화 됩니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)