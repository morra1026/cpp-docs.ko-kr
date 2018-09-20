---
title: '방법: 재정의 지정자 선언 (C + + /cli CLI) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- override specifiers in native compilation, overriding
ms.assetid: d0551836-9ac7-41eb-a6e9-a4b3ef60767d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 1089f2d9326cf268bd76ad59242e2664060b78fd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46386525"
---
# <a name="how-to-declare-override-specifiers-in-native-compilations-ccli"></a>방법: 네이티브 컴파일에 override 지정자 선언(C++/CLI)

[봉인](../windows/sealed-cpp-component-extensions.md), [추상](../windows/abstract-cpp-component-extensions.md), 및 [재정의](../windows/override-cpp-component-extensions.md) 사용 하지 않는 컴파일에 사용할 **/ZW** 또는 [/clr](../build/reference/clr-common-language-runtime-compilation.md)합니다.

> [!NOTE]
>  ISO C + + 11 표준 언어에는 [재정의](../cpp/override-specifier.md) 식별자와 [최종](../cpp/final-specifier.md) 식별자와 Visual Studio 사용에서을 지 `final` 대신 `sealed` 는 코드에서 네이티브 전용으로 컴파일됩니다.

## <a name="example"></a>예제

### <a name="description"></a>설명

다음 예에서는 `sealed` 네이티브 컴파일에 유효 합니다.

### <a name="code"></a>코드

```cpp
// sealed_native_keyword.cpp
#include <stdio.h>
__interface I1 {
   virtual void f();
   virtual void g();
};

class X : public I1 {
public:
   virtual void g() sealed {}
};

class Y : public X {
public:

   // the following override generates a compiler error
   virtual void g() {}   // C3248 X::g is sealed!
};
```

## <a name="example"></a>예제

### <a name="description"></a>설명

다음 예에서는 `override` 네이티브 컴파일에 유효 합니다.

### <a name="code"></a>코드

```cpp
// override_native_keyword.cpp
#include <stdio.h>
__interface I1 {
   virtual void f();
};

class X : public I1 {
public:
   virtual void f() override {}   // OK
   virtual void g() override {}   // C3668 I1::g does not exist
};
```

## <a name="example"></a>예제

### <a name="description"></a>설명

이 예에서는 `abstract` 네이티브 컴파일에 유효 합니다.

### <a name="code"></a>코드

```cpp
// abstract_native_keyword.cpp
class X abstract {};

int main() {
   X * MyX = new X;   // C3622 cannot instantiate abstract class
}
```

## <a name="see-also"></a>참고 항목

[Override 지정자](../windows/override-specifiers-cpp-component-extensions.md)