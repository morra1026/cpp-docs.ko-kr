---
title: 사용자 정의 특성 (C + + /cli 및 C + + /cli CX)
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- metadata, extending
- custom attributes, extending metadata
ms.assetid: 98b29048-a3ea-4698-8441-f149cdaec9fb
ms.openlocfilehash: f64cf5415e79678f0e0b43b58aae2249601fb3d7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50546655"
---
# <a name="user-defined-attributes--ccli-and-ccx"></a>사용자 정의 특성 (C + + /cli 및 C + + /cli CX)

C + + /cli 및 C + + /cli CX 인터페이스, 클래스 또는 구조체, 메서드, 매개 변수 또는 열거형의 메타 데이터를 확장 하는 플랫폼 특정 특성을 만들 수 있습니다. 이러한 특성은는 [표준 c + + 특성](../cpp/attributes.md)합니다.

## <a name="windows-runtime"></a>Windows 런타임

다음을 적용할 수 있습니다 C + + /cli CX 특성 속성에 있지만 생성자 또는 메서드 수는 없습니다.

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

## <a name="common-language-runtime"></a>공용 언어 런타임

에 표시 된 정보를 교체 하는 정보 및이 항목에 제시 된 구문 것 [특성](attributes/attribute.md)합니다.

줄어들고 형식을 정의 하 여 사용자 지정 특성을 정의할 수 있습니다 <xref:System.Attribute> 기본 클래스 형식 및 선택적으로 적용 합니다 <xref:System.AttributeUsageAttribute> 특성입니다.

자세한 내용은 다음을 참조하세요.

- [특성 대상](attribute-targets-cpp-component-extensions.md)

- [특성 매개 변수 형식](attribute-parameter-types-cpp-component-extensions.md)

Visual c + +에서 어셈블리 서명에 대 한 자세한 내용은 [강력한 이름 어셈블리 (어셈블리 서명) (C + + /cli CLI)](../dotnet/strong-name-assemblies-assembly-signing-cpp-cli.md)합니다.

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

다음 샘플에는 사용자 지정 특성을 정의 하는 방법을 보여 줍니다.

```cpp
// user_defined_attributes.cpp
// compile with: /clr /c
using namespace System;

[AttributeUsage(AttributeTargets::All)]
ref struct Attr : public Attribute {
   Attr(bool i){}
   Attr(){}
};

[Attr]
ref class MyClass {};
```

다음 예제에서는 사용자 지정 특성의 몇 가지 중요 한 기능을 보여 줍니다. 예를 들어, 사용자 지정 특성을 사용 하는 일반적인을 보여 주는이 예제: 완벽 하 게 클라이언트에 자체 설명할 수 있는 서버를 인스턴스화입니다.

```cpp
// extending_metadata_b.cpp
// compile with: /clr
using namespace System;
using namespace System::Reflection;

public enum class Access { Read, Write, Execute };

// Defining the Job attribute:
[AttributeUsage(AttributeTargets::Class, AllowMultiple=true )]
public ref class Job : Attribute {
public:
   property int Priority {
      void set( int value ) { m_Priority = value; }
      int get() { return m_Priority; }
   }

   // You can overload constructors to specify Job attribute in different ways
   Job() { m_Access = Access::Read; }
   Job( Access a ) { m_Access = a; }
   Access m_Access;

protected:
   int m_Priority;
};

interface struct IService {
   void Run();
};

   // Using the Job attribute:
   // Here we specify that QueryService is to be read only with a priority of 2.
   // To prevent namespace collisions, all custom attributes implicitly
   // end with "Attribute".

[Job( Access::Read, Priority=2 )]
ref struct QueryService : public IService {
   virtual void Run() {}
};

// Because we said AllowMultiple=true, we can add multiple attributes
[Job(Access::Read, Priority=1)]
[Job(Access::Write, Priority=3)]
ref struct StatsGenerator : public IService {
   virtual void Run( ) {}
};

int main() {
   IService ^ pIS;
   QueryService ^ pQS = gcnew QueryService;
   StatsGenerator ^ pSG = gcnew StatsGenerator;

   //  use QueryService
   pIS = safe_cast<IService ^>( pQS );

   // use StatsGenerator
   pIS = safe_cast<IService ^>( pSG );

   // Reflection
   MemberInfo ^ pMI = pIS->GetType();
   array <Object ^ > ^ pObjs = pMI->GetCustomAttributes(false);

   // We can now quickly and easily view custom attributes for an
   // Object through Reflection */
   for( int i = 0; i < pObjs->Length; i++ ) {
      Console::Write("Service Priority = ");
      Console::WriteLine(static_cast<Job^>(pObjs[i])->Priority);
      Console::Write("Service Access = ");
      Console::WriteLine(static_cast<Job^>(pObjs[i])->m_Access);
   }
}
```

```Output
Service Priority = 0

Service Access = Write

Service Priority = 3

Service Access = Write

Service Priority = 1

Service Access = Read
```

`Object^` 형식이 variant 데이터 형식을 대체 합니다. 다음 예제에서는 배열을 사용 하는 사용자 지정 특성을 정의 `Object^` 매개 변수로 합니다.

특성 인수에는 컴파일 시간 상수; 여야 합니다. 대부분의 경우에서 상수 리터럴 여야 합니다.

참조 [typeid](typeid-cpp-component-extensions.md) 사용자 지정 특성 블록에서 system:: type 값을 반환 하는 방법에 대 한 정보에 대 한 합니다.

```cpp
// extending_metadata_e.cpp
// compile with: /clr /c
using namespace System;
[AttributeUsage(AttributeTargets::Class | AttributeTargets::Method)]
public ref class AnotherAttr : public Attribute {
public:
   AnotherAttr(array<Object^>^) {}
   array<Object^>^ var1;
};

// applying the attribute
[ AnotherAttr( gcnew array<Object ^> { 3.14159, "pi" }, var1 = gcnew array<Object ^> { "a", "b" } ) ]
public ref class SomeClass {};
```

런타임에 사용자 지정 특성 클래스의 공개 부분을 직렬화 해야 필요 합니다.  사용자 지정 특성을 작성할 때 사용자 지정 특성의 명명 된 인수는 컴파일 시간 상수 제한 됩니다.  (생각할 클래스 레이아웃 메타 데이터에 추가 된 비트의 시퀀스입니다.)

```cpp
// extending_metadata_f.cpp
// compile with: /clr /c
using namespace System;
ref struct abc {};

[AttributeUsage( AttributeTargets::All )]
ref struct A : Attribute {
   A( Type^ ) {}
   A( String ^ ) {}
   A( int ) {}
};

[A( abc::typeid )]
ref struct B {};
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP용 구성 요소 확장](component-extensions-for-runtime-platforms.md)