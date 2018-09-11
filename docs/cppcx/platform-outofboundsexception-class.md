---
title: 'Platform:: outofboundsexception 클래스 | Microsoft Docs'
ms.custom: ''
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.topic: reference
f1_keywords:
- VCCORLIB/Platform::OutOfBoundsException
- VCCORLIB/Platform::OutOfBoundsException::OutOfBoundsException
dev_langs:
- C++
helpviewer_keywords:
- Platform::OutOfBoundsException
ms.assetid: 96f8bf75-1207-4049-964b-7771822cadf3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e1a7fad8f4d0bdc0c91dab50f5737b6aa4476438
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44105772"
---
# <a name="platformoutofboundsexception-class"></a>Platform::OutOfBoundsException 클래스

작업이 유효한 범위를 벗어난 데이터에 액세스하려고 하면 throw됩니다.

## <a name="syntax"></a>구문

```cpp
public ref class OutOfBoundsException : COMException,    IException,    IPrintable,    IEquatable
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