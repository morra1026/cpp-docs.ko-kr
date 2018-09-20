---
title: 'MakeAllocator:: ~ MakeAllocator 소멸자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::MakeAllocator::~MakeAllocator
dev_langs:
- C++
helpviewer_keywords:
- ~MakeAllocator, destructor
ms.assetid: f1299c5f-cc6b-4d4e-85d4-aee1be0e2b0a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5ba40aa98321956f19de30f5f4002cb788ff446e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46371994"
---
# <a name="makeallocatormakeallocator-destructor"></a>MakeAllocator::~MakeAllocator 소멸자

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
~MakeAllocator();
```

## <a name="remarks"></a>설명

현재 인스턴스 초기화를 해제 합니다 **MakeAllocator** 클래스입니다.

이 소멸자는 또한 필요한 경우 할당된 된 기본 메모리를 삭제 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[MakeAllocator 클래스](../windows/makeallocator-class.md)<br/>
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)