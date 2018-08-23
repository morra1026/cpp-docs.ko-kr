---
title: 'Mutex:: mutex 생성자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Mutex::Mutex
dev_langs:
- C++
helpviewer_keywords:
- Mutex, constructor
ms.assetid: 504afcdc-775a-4c98-a06f-4fb4663eba3f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 62a1fc796188c38dfbd3aff004eba15b7e30ea89
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42600507"
---
# <a name="mutexmutex-constructor"></a>Mutex::Mutex 생성자

새 인스턴스를 초기화 합니다 **뮤텍스** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
explicit Mutex(
   HANDLE h
);

Mutex(
   _Inout_ Mutex&& h
);
```

### <a name="parameters"></a>매개 변수

*h*  
핸들 또는 rvalue 참조 핸들을 하는 **뮤텍스** 개체입니다.

## <a name="remarks"></a>설명

첫 번째 생성자는 초기화 된 **뮤텍스** 지정된 된 핸들에서 개체입니다. 두 번째 생성자는 초기화 된 **뮤텍스** 현재 개체와 지정 된 핸들을 다음 뮤텍스의 소유권 이동 **뮤텍스** 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목
[Mutex 클래스](../windows/mutex-class1.md)