---
title: Platform::SizeT 값 클래스
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/PlatformSizeT::SizeT constructor
helpviewer_keywords:
- Platform::SizeT Struct
ms.assetid: 0803612c-8ba1-430c-9b7b-1bebae88608d
ms.openlocfilehash: 02fe62165ce40d267f156eaeb3ad93f636c9ab73
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50604219"
---
# <a name="platformsizet-value-class"></a>Platform::SizeT 값 클래스

개체의 크기를 나타냅니다. SizeT는 부호 없는 데이터 형식입니다.

## <a name="syntax"></a>구문

```cpp
public ref class SizeT sealed : ValueType
```

### <a name="members"></a>멤버

|멤버|설명|
|------------|-----------------|
|[SizeT::SizeT 생성자](#ctor)|지정된 값을 사용하여 클래스의 새 인스턴스를 초기화합니다.|

### <a name="requirements"></a>요구 사항

**지원 되는 최소 클라이언트:** Windows 8

**지원 되는 최소 서버:** Windows Server 2012

**네임스페이스:** Platform

**메타데이터:** platform.winmd

## <a name="ctor"></a>  Sizet:: Sizet 생성자

지정된 값을 사용하여 SizeT의 새 인스턴스를 초기화합니다.

### <a name="syntax"></a>구문

```cpp
SizeT( uint32 value1 );   SizeT( void* value2 );
```

### <a name="parameters"></a>매개 변수

*Value1*<br/>
부호 없는 32비트 값입니다.

*Value2*<br/>
부호 없는 32비트 값에 대한 포인터입니다.

## <a name="see-also"></a>참고 항목

[Platform 네임 스페이스](../cppcx/platform-namespace-c-cx.md)