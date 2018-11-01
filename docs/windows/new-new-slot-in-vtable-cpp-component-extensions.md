---
title: 새 (새 vtable의 슬롯) (C + + /cli 및 C + + /cli CX)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- new keyword [C++]
ms.assetid: 1a9a5704-f02f-46ae-ad65-f0f2b6dbabc3
ms.openlocfilehash: b143b2ead1165382d0959f4e4c90f1d2e7ea936a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50487167"
---
# <a name="new-new-slot-in-vtable--ccli-and-ccx"></a>새 (새 vtable의 슬롯) (C + + /cli 및 C + + /cli CX)

합니다 **새** 키워드를 가상 멤버가 vtable의 new 슬롯을 얻게 되며 나타냅니다.

## <a name="all-runtimes"></a>모든 런타임

(이 언어 기능에는 모든 런타임에 적용되는 설명이 없습니다.)

## <a name="windows-runtime"></a>Windows 런타임

Windows 런타임에서 지원 되지 않습니다.

## <a name="common-language-runtime"></a>공용 언어 런타임

### <a name="remarks"></a>설명

에 `/clr` 컴파일 **새** 가상 멤버가 vtable의 new 슬롯을 얻게 되며, 함수가 기본 클래스 메서드를 재정의 하지 않습니다 나타냅니다.

**새** 함수에 대 한 IL에 추가할 새 슬롯 한정자를 사용 하면 됩니다.  새 슬롯에 대 한 자세한 내용은 다음을 참조 하세요.

- [MethodInfo.GetBaseDefinition 메서드](https://msdn.microsoft.com/library/system.reflection.methodinfo.getbasedefinition.aspx)

- [메서드에 열거형](https://msdn.microsoft.com/library/system.reflection.methodattributes.aspx)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

다음 샘플의 결과 보여 줍니다 **새**합니다.

```cpp
// newslot.cpp
// compile with: /clr
ref class C {
public:
   virtual void f() {
      System::Console::WriteLine("C::f() called");
   }

   virtual void g() {
      System::Console::WriteLine("C::g() called");
   }
};

ref class D : public C {
public:
   virtual void f() new {
      System::Console::WriteLine("D::f() called");
   }

   virtual void g() override {
      System::Console::WriteLine("D::g() called");
   }
};

ref class E : public D {
public:
   virtual void f() override {
      System::Console::WriteLine("E::f() called");
   }
};

int main() {
   D^ d = gcnew D;
   C^ c = gcnew D;

   c->f();   // calls C::f
   d->f();   // calls D::f

   c->g();   // calls D::g
   d->g();   // calls D::g

   D ^ e = gcnew E;
   e->f();   // calls E::f
}
```

```Output
C::f() called

D::f() called

D::g() called

D::g() called

E::f() called
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)<br/>

[Override 지정자](../windows/override-specifiers-cpp-component-extensions.md)