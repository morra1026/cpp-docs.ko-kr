---
title: ActivatableClass 매크로
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ActivatableClass
- ActivatableClassWithFactory
- ActivatableClassWithFactoryEx
helpviewer_keywords:
- ActivatableClassWithFactory
- ActivatableClass
- ActivatableClassWithFactoryEx
ms.assetid: 9bd64709-ec2c-4678-8c96-ea5982622bdd
ms.openlocfilehash: eee8267e2e76eead267eb2486836dbcc38a90231
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336606"
---
# <a name="activatableclass-macros"></a>ActivatableClass 매크로

지정된 된 클래스의 인스턴스를 만들 수 있는 팩터리를 포함 하는 내부 캐시를 채웁니다.

## <a name="syntax"></a>구문

```cpp
ActivatableClass(
   className
);

ActivatableClassWithFactory(
   className,
   factory
);

ActivatableClassWithFactoryEx(
   className,
   factory,
   serverName
);
```

### <a name="parameters"></a>매개 변수

*className*<br/>
만들 클래스의 이름입니다.

*factory*<br/>
지정된 된 클래스의 인스턴스를 만든 팩터리입니다.

*serverName*<br/>
모듈의 팩터리 하위 집합을 지정 하는 이름입니다.

## <a name="remarks"></a>설명

사용 하지 않는 경우 클래식 COM을 사용 하 여 이러한 매크로 사용 하지 마십시오 합니다 `#undef` 되도록 지시문을 `__WRL_WINRT_STRICT__` 매크로 정의 제거 됩니다.

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Module 클래스](module-class.md)