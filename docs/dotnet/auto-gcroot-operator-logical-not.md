---
title: auto_gcroot::operator! | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- msclr.auto_gcroot.operator!
- auto_gcroot.operator!
- msclr::auto_gcroot::operator!
- auto_gcroot::operator!
dev_langs:
- C++
helpviewer_keywords:
- auto_gcroot::operator!
ms.assetid: f9728be3-2e09-4c01-a594-43e0d59d40d3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: d470974a6f50f7040a46a3f64f9fd431e2796545
ms.sourcegitcommit: 8480f16893f09911f08a58caf684405404f7ac8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49161374"
---
# <a name="autogcrootoperator"></a>auto_gcroot::operator!

연산자를 사용 하 여 `auto_gcroot` 조건식에서입니다.

## <a name="syntax"></a>구문

```
bool operator!() const;
```

## <a name="return-value"></a>반환 값

**true** 래핑된 개체가 잘못 된 경우 **false** 그렇지 않은 경우.

## <a name="example"></a>예제

```cpp
// msl_auto_gcroot_operator_not.cpp
// compile with: /clr
#include <msclr\auto_gcroot.h>

using namespace System;
using namespace msclr;

int main() {
   auto_gcroot<String^> s;
   if ( s ) Console::WriteLine( "s is valid" );
   if ( !s ) Console::WriteLine( "s is invalid" );
   s = "something";
   if ( s ) Console::WriteLine( "now s is valid" );
   if ( !s ) Console::WriteLine( "now s is invalid" );
   s.reset();
   if ( s ) Console::WriteLine( "now s is valid" );
   if ( !s ) Console::WriteLine( "now s is invalid" );
}
```

```Output
s is invalid
now s is valid
now s is invalid
```

## <a name="requirements"></a>요구 사항

**헤더 파일** \<msclr\auto_gcroot.h >

**Namespace** msclr

## <a name="see-also"></a>참고 항목

[auto_gcroot 멤버](../dotnet/auto-gcroot-members.md)<br/>
[auto_gcroot::operator bool](../dotnet/auto-gcroot-operator-bool.md)