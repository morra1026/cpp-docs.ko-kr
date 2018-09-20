---
title: 'Event:: event 생성자 (Windows Runtime c + + 템플릿 라이브러리) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Event::Event
dev_langs:
- C++
ms.assetid: 21495297-9612-4095-9256-16e168cc0021
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 8bd9f02935d0d88976fd3b62c7276f106519fa74
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46381012"
---
# <a name="eventevent-constructor-windows-runtime-c-template-library"></a>Event::Event 생성자(Windows Runtime C++ 템플릿 라이브러리)

새 인스턴스를 초기화 합니다 **이벤트** 클래스입니다.

## <a name="syntax"></a>구문

```cpp
explicit Event(
   HANDLE h = HandleT::Traits::GetInvalidValue()  
);
WRL_NOTHROW Event(
   _Inout_ Event&& h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
이벤트에 대한 핸들. 기본적으로 *h* 으로 초기화 됩니다 **nullptr**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[Event 클래스(Windows Runtime C++ 템플릿 라이브러리)](../windows/event-class-windows-runtime-cpp-template-library.md)