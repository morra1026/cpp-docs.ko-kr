---
title: 재정의 (C + + /cli 및 C + + /cli CX)
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- overriding, override keyword [C++]
- override keyword [C++]
ms.assetid: 34d19257-1686-4fcd-96f5-af07c70ba914
ms.openlocfilehash: be7a347e4ddc700acaf4c5a968af648195445485
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50647371"
---
# <a name="override--ccli-and-ccx"></a>재정의 (C + + /cli 및 C + + /cli CX)

합니다 **재정의** 상황에 맞는 키워드는 형식의 멤버를 기본 클래스 또는 기본 인터페이스 멤버를 재정의 함을 나타냅니다.

## <a name="remarks"></a>설명

**재정의** 키워드는 네이티브 대상 (기본 컴파일러 옵션)을 컴파일할 때 올바른 Windows 런타임 대상 (`/ZW` 컴파일러 옵션), 또는 공용 언어 런타임 대상을 (`/clr` 컴파일러 옵션).

재정의 지정자에 대 한 자세한 내용은 참조 하세요. [재정의 지정자](../cpp/override-specifier.md) 하 고 [재정의 지정자 및 네이티브 컴파일](../dotnet/how-to-declare-override-specifiers-in-native-compilations-cpp-cli.md)합니다.

상황에 맞는 키워드에 대 한 자세한 내용은 참조 하세요. [상황에 맞는 키워드](../windows/context-sensitive-keywords-cpp-component-extensions.md)합니다.

## <a name="examples"></a>예제

다음 코드 예제에 따르면 **재정의** 네이티브 컴파일에 사용할 수도 있습니다.

```cpp
// override_keyword_1.cpp
// compile with: /c
struct I1 {
   virtual void f();
};

struct X : public I1 {
   virtual void f() override {}
};
```

### <a name="example"></a>예제

다음 코드 예제에 따르면 **재정의** Windows 런타임 컴파일에서 사용할 수 있습니다.

```cpp
// override_keyword_2.cpp
// compile with: /ZW /c
ref struct I1 {
   virtual void f();
};

ref struct X : public I1 {
   virtual void f() override {}
};
```

#### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

### <a name="example"></a>예제

다음 코드 예제에 따르면 **재정의** 공용 언어 런타임 컴파일에서 사용할 수 있습니다.

```cpp
// override_keyword_3.cpp
// compile with: /clr /c
ref struct I1 {
   virtual void f();
};

ref struct X : public I1 {
   virtual void f() override {}
};
```

#### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

## <a name="see-also"></a>참고 항목

[override 지정자](../cpp/override-specifier.md)<br/>
[Override 지정자](../windows/override-specifiers-cpp-component-extensions.md)