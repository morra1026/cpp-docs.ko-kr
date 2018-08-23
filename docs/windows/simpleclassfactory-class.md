---
title: SimpleClassFactory 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::SimpleClassFactory
dev_langs:
- C++
helpviewer_keywords:
- SimpleClassFactory class
ms.assetid: 6edda1b2-4e44-4e14-9364-72f519249962
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: deb100cfcbb8d2af14501b8b5cf90569a90c2d4d
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42600493"
---
# <a name="simpleclassfactory-class"></a>SimpleClassFactory 클래스

기본 클래스를 만드는 기본적인 메커니즘을 제공합니다.

## <a name="syntax"></a>구문

```cpp
template<typename Base>
class SimpleClassFactory : public ClassFactory<>;
```

### <a name="parameters"></a>매개 변수

*자료*  
기본 클래스입니다.

## <a name="remarks"></a>설명

기본 클래스 기본 생성자를 제공 해야 합니다.

다음 코드 예제에 사용 하는 방법을 보여 줍니다 **SimpleClassFactory** 사용 하 여 합니다 [ActivatableClassWithFactoryEx](../windows/activatableclass-macros.md) 매크로입니다.

`ActivatableClassWithFactoryEx(MyClass, SimpleClassFactory, MyServerName);`

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

|이름|설명|
|----------|-----------------|
|[SimpleClassFactory::CreateInstance 메서드](../windows/simpleclassfactory-createinstance-method.md)|지정된 된 인터페이스의 인스턴스를 만듭니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`I0`

`ChainInterfaces`

`I0`

`RuntimeClassBase`

`ImplementsHelper`

`DontUseNewUseMake`

`RuntimeClassFlags`

`RuntimeClassBaseT`

`RuntimeClass`

`ClassFactory`

`SimpleClassFactory`

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)