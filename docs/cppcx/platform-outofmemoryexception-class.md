---
title: Platform::OutOfMemoryException 클래스
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::OutOfMemoryException
- VCCORLIB/Platform::OutOfMemoryException::OutOfMemoryException
helpviewer_keywords:
- Platform::OutOfMemoryException
ms.assetid: 49c19f6b-f66c-4448-b861-91dcbf32de2c
ms.openlocfilehash: bf13e1589f651b7791fe67f6061b06b1a0bd897f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50478184"
---
# <a name="platformoutofmemoryexception-class"></a>Platform::OutOfMemoryException 클래스

메모리가 부족하여 작업을 완료할 수 없는 경우 throw됩니다.

## <a name="syntax"></a>구문

```cpp
public ref class OutOfMemoryException : COMException,    IException,    IPrintable,    IEquatable
```

### <a name="remarks"></a>설명

자세한 내용은 [COMException](../cppcx/platform-comexception-class.md) 클래스를 참조하세요.

### <a name="requirements"></a>요구 사항

**지원 되는 최소 클라이언트:** Windows 8

**지원 되는 최소 서버:** Windows Server 2012

**네임스페이스:** Platform

**메타데이터:** platform.winmd

## <a name="see-also"></a>참고 항목

[Platform::COMException 클래스](../cppcx/platform-comexception-class.md)