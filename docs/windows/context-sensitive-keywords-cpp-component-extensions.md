---
title: 상황에 맞는 키워드 (C + + /cli 및 C + + /cli CX) | Microsoft Docs
ms.custom: ''
ms.date: 10/12/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- internal_CPP
dev_langs:
- C++
helpviewer_keywords:
- context-sensitive keywords
ms.assetid: e33da089-f434-44e9-8cce-4668d05a8939
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5d02939e61da4a247b46da5637c38d01e7990c49
ms.sourcegitcommit: 3f4e92266737ecb70507871e87dc8e2965ad7e04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49327936"
---
# <a name="context-sensitive-keywords--ccli-and-ccx"></a>상황에 맞는 키워드 (C + + /cli 및 C + + /cli CX)

*상황에 맞는 키워드* 는 특정 컨텍스트에서만에서 인식 되는 언어 요소입니다. 특정 컨텍스트가 아닐 경우 상황에 맞는 키워드는 사용자 정의 기호일 수 있습니다.

## <a name="all-runtimes"></a>모든 런타임

### <a name="remarks"></a>설명

다음은 상황에 맞는 키워드의 목록입니다.

- [abstract](../windows/abstract-cpp-component-extensions.md)

- [delegate](../windows/delegate-cpp-component-extensions.md)

- [event](../windows/event-cpp-component-extensions.md)

- [finally](../dotnet/finally.md)

- [for each, in](../dotnet/for-each-in.md)

- [initonly](../dotnet/initonly-cpp-cli.md)

- `internal`

- [name](../windows/literal-cpp-component-extensions.md)

- [override](../windows/override-cpp-component-extensions.md)

- [속성](../windows/property-cpp-component-extensions.md)

- [sealed](../windows/sealed-cpp-component-extensions.md)

- `where` (부분 [제네릭](../windows/generics-cpp-component-extensions.md))

가독성을 위해 사용자 정의 기호로 상황에 맞는 키워드의 사용을 제한 하는 것이 좋습니다.

## <a name="windows-runtime"></a>Windows 런타임

### <a name="remarks"></a>설명

(이 기능에는 플랫폼별 설명이 없습니다.)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

## <a name="common-language-runtime"></a>공용 언어 런타임

### <a name="remarks"></a>설명

(이 기능에는 플랫폼별 설명이 없습니다.)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

다음 코드 예제는 적절 한 컨텍스트에서 따르면 합니다 **속성** 속성 및 변수를 정의 하는 상황에 맞는 키워드를 사용할 수 있습니다.

```cpp
// context_sensitive_keywords.cpp
// compile with: /clr
public ref class C {
   int MyInt;
public:
   C() : MyInt(99) {}

   property int Property_Block {   // context-sensitive keyword
      int get() { return MyInt; }
   }
};

int main() {
   int property = 0;               // variable name
   C ^ MyC = gcnew C();
   property = MyC->Property_Block;
   System::Console::WriteLine(++property);
}
```

```Output
100
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP 용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)