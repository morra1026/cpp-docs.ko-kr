---
title: Platform::Delegate 클래스
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::Delegate
helpviewer_keywords:
- Platform::Delegate Class
ms.assetid: 82b21271-768f-4193-9ca2-be68ddfd546e
ms.openlocfilehash: 6a509827b3b8e14b6d28995b5b4ca468ee9a662e
ms.sourcegitcommit: dedd4c3cb28adec3793329018b9163ffddf890a4
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2019
ms.locfileid: "57741178"
---
# <a name="platformdelegate-class"></a>Platform::Delegate 클래스

함수 개체를 나타냅니다.

## <a name="syntax"></a>구문

```cpp
public delegate void delegate_name();
```

### <a name="members"></a>멤버

Delegate 클래스에는 [Platform::Object Class](../cppcx/platform-object-class.md)에서 파생된 Equals(), GetHashCode() 및 ToString() 메서드가 있습니다.

### <a name="remarks"></a>설명

[delegate](../windows/delegate-cpp-component-extensions.md) 키워드를 사용하여 대리자를 만듭니다. Platform::Delegate를 명시적으로 사용하지 마세요. 자세한 내용은 [대리자](../cppcx/delegates-c-cx.md)를 참조하세요. 대리자를 만들고 사용하는 방법에 대한 예제는 [Creating Windows Runtime Components in C++](/windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp)를 참조하세요.

### <a name="requirements"></a>요구 사항

**지원 되는 최소 클라이언트:** Windows 8

**지원 되는 최소 서버:** Windows Server 2012

**네임스페이스:** 플랫폼

**메타데이터:** platform.winmd

## <a name="see-also"></a>참고자료

[Platform 네임 스페이스](../cppcx/platform-namespace-c-cx.md)
