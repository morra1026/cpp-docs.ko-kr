---
title: auto_gcroot::operator bool
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- auto_gcroot.operator bool
- auto_gcroot::operator bool
- msclr.auto_gcroot.operator bool
- msclr::auto_gcroot::operator bool
- operator bool
helpviewer_keywords:
- bool operator
ms.assetid: 87d38498-4221-4de8-8d02-c2dd2e6274ec
ms.openlocfilehash: f07cd378eea9c68542a50b579b9aff17ec2b3693
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50659357"
---
# <a name="autogcrootoperator-bool"></a>auto_gcroot::operator bool

연산자를 사용 하 여 `auto_gcroot` 조건식에서입니다.

## <a name="syntax"></a>구문

```
operator bool() const;
```

## <a name="return-value"></a>반환 값

**true** 래핑된 개체가 잘못 되었습니다. **false** 그렇지 않은 경우.

## <a name="remarks"></a>설명

이 연산자를 실제로 변환 `_detail_class::_safe_bool` 는 보다 안전한 **bool** 정수 계열 형식으로 변환할 수 없기 때문입니다.

## <a name="example"></a>예제

```cpp
// msl_auto_gcroot_operator_bool.cpp
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
[auto_gcroot::operator!](../dotnet/auto-gcroot-operator-logical-not.md)