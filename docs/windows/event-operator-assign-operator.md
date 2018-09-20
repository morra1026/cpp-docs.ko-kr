---
title: 'Event:: operator = 연산자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Event::operator=
dev_langs:
- C++
helpviewer_keywords:
- operator= operator
ms.assetid: d8fe9820-8856-4899-9553-56226bdc4945
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 072d4af94e4889d49d9b4876daa27cb4801d60d0
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46447013"
---
# <a name="eventoperator-operator"></a>Event::operator= 연산자

지정 된 할당 **이벤트** 현재 참조 **이벤트** 인스턴스.

## <a name="syntax"></a>구문

```cpp
WRL_NOTHROW Event& operator=(
   _Inout_ Event&& h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
rvalue 참조를 **이벤트** 인스턴스.

## <a name="return-value"></a>반환 값

현재 포인터 **이벤트** 인스턴스.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[Event 클래스(Windows Runtime C++ 템플릿 라이브러리)](../windows/event-class-windows-runtime-cpp-template-library.md)