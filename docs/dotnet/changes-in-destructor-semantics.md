---
title: 소멸자 의미의 변경 내용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- finalizers [C++]
- destructors, C++
ms.assetid: f1869944-a407-452f-b99a-04d8c209f0dc
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: c25045291afed1e8072867ee668716b2f396ef30
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46420025"
---
# <a name="changes-in-destructor-semantics"></a>소멸자 의미의 변경 내용

클래스 소멸자에 대 한 의미 체계는 Visual c + +는 데 Managed Extensions for c + + 크게 변경 되었습니다.

Managed Extensions 클래스 소멸자 값 클래스 내부가 아니라 참조 클래스 내에서 허용 되었습니다. 이 새 구문에서 변경 되지 않았습니다. 그러나 클래스 소멸자의 의미 체계 변경 되었습니다. 이 항목에 중점을 둡니다 이유를 변경 하 고 기존 CLR 코드 변환에 미치는 영향에 대해 설명 합니다. 언어의 두 버전 간의 가장 중요 한 프로그래머 수준의 변경 때문일 수 있습니다.

## <a name="non-deterministic-finalization"></a>비 결정적인 종료

가비지 수집기에 연결된 하 여 개체에 연결 된 메모리를 회수 하기 전에 `Finalize` 메서드가 있는 경우 호출 됩니다. 개체의 프로그램 수명과 연결 되지 않은 때문에 상위 소멸자 형태의이 메서드의 생각할 수 있습니다. 종료로이 참조합니다. 타이밍 또는 있는지 여부를 `Finalize` 메서드 정의 되지 않습니다. 말, 가비지 수집에서는 비결 종료를 수행 한다는 의미입니다.

비결 종료 동적 메모리 관리와 잘 작동합니다. 사용 가능한 메모리가 부족 한 면 가비지 수집기를 시작 합니다. 가비지 수집 환경 소멸자 사용 가능한 메모리를 필요 하지 않습니다. 하지만 비결 종료 작동 하지 않습니다, 개체가 데이터베이스 연결 또는 일종의 잠금 같은 중요 한 리소스를 유지 하는 경우. 이 경우 가능한 한 빨리 해당 리소스를 해제 해야 했습니다. 생성자/소멸자 쌍을 사용 하 여 달성 된 네이티브 환경입니다. 개체의 수명이 종료 되는 즉시 로컬 선언 된 블록이 종료 될 때 또는 스택 throw 된 예외를 끝나거나 때 소멸자가 실행 하 고 리소스가 자동으로 해제 됩니다. 이 방법은 매우 및 Managed extensions 부재 찾기가 누락 되었습니다.

구현 하는 클래스에 대 한 CLR에서 제공 하는 솔루션은는 `Dispose` 메서드는 `IDisposable` 인터페이스입니다. 여기서 문제는 `Dispose` 사용자가 명시적 호출 해야 합니다. 이 오류가 발생 하기 쉽습니다. C# 언어에서 특별 한 형태의 자동화 어느 정도의 제공 `using` 문입니다. Managed Extensions 디자인 없는 특별 한 지원을 제공합니다.

## <a name="destructors-in-managed-extensions-for-c"></a>Managed Extensions for c + +의 소멸자

Managed Extensions에서 참조 클래스의 소멸자는 다음 두 단계를 사용 하 여 구현 됩니다.

1. 사용자가 제공한 소멸자에 내부적으로 이름이 `Finalize`합니다. 클래스에 기본 클래스가 있는 경우 (기억에 CLR 개체 모델에서 단일 상속만 지원 됩니다), 컴파일러 해당 종료자 사용자 제공 코드의 실행에 대 한 호출을 삽입 합니다. 예를 들어 Managed Extensions 언어 사양에서 가져온 다음 간단한 계층 구조를 고려 합니다.

```
__gc class A {
public:
   ~A() { Console::WriteLine(S"in ~A"); }
};

__gc class B : public A {
public:
   ~B() { Console::WriteLine(S"in ~B");  }
};
```

이 예제에서는 두 소멸자 이름이 `Finalize`합니다. `B``Finalize` 호출에 `A`의 `Finalize` 호출 뒤에 추가 메서드가 `WriteLine`합니다. 이 새로운 가비지 수집기는 기본적으로 호출 종료 중입니다. 이 내부 변환의 모양을 다음과 같습니다.

```
// internal transformation of destructor under Managed Extensions
__gc class A {
public:
   void Finalize() { Console::WriteLine(S"in ~A"); }
};

__gc class B : public A {
public:
   void Finalize() {
      Console::WriteLine(S"in ~B");
      A::Finalize();
   }
};
```

1. 두 번째 단계에서는 가상 소멸자를 합성 하는 컴파일러입니다. 이 소멸자는 Managed Extensions 사용자 프로그램 직접적으로 또는 delete 식의 응용 프로그램을 통해 호출 합니다. 가비지 수집기에 의해 호출 되지 않습니다.

     두 개의 문이이 합성 된 소멸자 내에 배치 됩니다. 하나는에 대 한 호출 `GC::SuppressFinalize` 더 이상 없는 호출 되었는지 확인 하려면 `Finalize`합니다. 두 번째는 실제로 호출 `Finalize`, 해당 클래스에 대 한 사용자가 제공한 소멸자 나타냅니다. 이 모양을 다음과 같습니다.

```
__gc class A {
public:
   virtual ~A() {
      System::GC::SuppressFinalize(this);
      A::Finalize();
   }
};

__gc class B : public A {
public:
   virtual ~B() {
      System::GC::SuppressFinalize(this);
      B::Finalize();
   }
};
```

이 이것을 사용 하면 명시적으로 클래스를 호출 하는 동안 `Finalize` 메서드가 이제 대신, 제어할 수 없는 시간에이 연결 되지 않으므로 실제로 사용 하 여는 `Dispose` 메서드 솔루션입니다. 이 Visual c + +에서 변경 됩니다.

## <a name="destructors-in-new-syntax"></a>새 구문에서 소멸자

새 구문에서 소멸자 이름이 내부적으로 `Dispose` 메서드 및 참조 클래스 구현에 자동으로 확장 되는 `IDispose` 인터페이스. 즉, Visual c + +, 살펴본 클래스 쌍 변환 다음과 같이 합니다.

```
// internal transformation of destructor under the new syntax
__gc class A : IDisposable {
public:
   void Dispose() {
      System::GC::SuppressFinalize(this);
      Console::WriteLine( "in ~A");
   }
};

__gc class B : public A {
public:
   void Dispose() {
      System::GC::SuppressFinalize(this);
      Console::WriteLine( "in ~B");
      A::Dispose();
   }
};
```

새 구문 중 하나는 소멸자가 명시적으로 호출 하거나 `delete` 기본 추적 핸들을 적용할 `Dispose` 메서드는 자동으로 호출 됩니다. 파생된 클래스의 호출을 인지 합니다 `Dispose` 기본 클래스의 메서드 종료 시에 합성 된 메서드의 삽입 됩니다.

그러나이 않습니다 하지 명확한 종료 방법. 이 위해서는 로컬 참조 개체의 한 추가 지원이 필요 합니다. (이 관리 되는 확장 내에서 유사한 지원 되지 않습니다 및 따라서 이것은 변환 문제)

## <a name="declaring-a-reference-object"></a>참조 개체를 선언합니다.

Visual c + +에서는 선언 참조 클래스 개체의 로컬 스택에 하거나 클래스의 구성원으로 직접 액세스할 수 있는 것 처럼 합니다. 가진 소멸자의 연결을 함께 사용 하면를 `Dispose` 메서드 결과 참조 형식에 종료 의미 체계의 자동화 된 호출 합니다.

첫째, 클래스 생성자를 통해 리소스를 확보도 개체를 만드는 함수는 참조 클래스를 정의 합니다. 둘째, 클래스 소멸자 내에서 개체를 만들 때 얻은 리소스를 해제 했습니다.

```
public ref class R {
public:
   R() { /* acquire expensive resource */ }
   ~R() { /* release expensive resource */ }

   // everything else...
};
```

개체는 괄호 없이 형식 이름을 사용 하 여 로컬로 선언 됩니다. 메서드를 호출 하는 등 개체의 모든 사용 멤버 선택 점 통해 수행 됩니다 (`.`) 대신 화살표 (`->`). 블록의 끝으로 변환 하는 연결 된 소멸자가 `Dispose`, 다음과 같이 자동으로 호출 됩니다.

```
void f() {
   R r;
   r.methodCall();

   // r is automatically destructed here -
   // that is, r.Dispose() is invoked
}
```

마찬가지로 `using` 문 내에서 C#이 모든 참조 형식이 기본 CLR 제약 조건이 없습니다 질문도지 않습니다 CLR 힙에 할당 해야 합니다. 기본 의미 체계가 변경 되지 않습니다. 사용자 수 동등 하 게 기록한 다음 (및이 컴파일러에서 수행한 내부 변환):

```
// equivalent implementation
// except that it should be in a try/finally clause
void f() {
   R^ r = gcnew R;
   r->methodCall();

   delete r;
}
```

실제로 새 구문에서 소멸자 다시 쌍을 이루는 생성자는 자동화 된 취득/릴리스로 메커니즘 로컬 개체의 수명에 연결 합니다.

## <a name="declaring-an-explicit-finalize"></a>명시적 종료를 선언합니다.

새 구문에서 앞서 설명한 것 처럼 소멸자는으로 합성 합니다 `Dispose` 메서드. 즉, 않는 소멸자가 명시적으로 호출 되지 경우 가비지 수집기에 종료 하는 동안 이전과 찾지 못합니다 연결 된 `Finalize` 메서드는 개체에 대 한 합니다. 소멸 및 종료를 지원 하려면 종료자를 제공 하기 위한 특수 구문을 도입 했습니다. 예를 들어:

```
public ref class R {
public:
   !R() { Console::WriteLine( "I am the R::finalizer()!" ); }
};
```

합니다 `!` 물결표 접두사 비슷합니다 (`~`) 클래스 소멸자는-즉, 모두 후 수명 메서드에 있는 클래스의 이름 토큰입니다. 경우는 합성 `Finalize` 메서드 호출 기본 클래스의 파생된 클래스 내에서 발생 `Finalize` 메서드 끝에 삽입 됩니다. 소멸자가 명시적으로 호출 하는 경우 종료 자가 표시 되지 않습니다. 변환 모양을 다음과 같습니다.

```
// internal transformation under new syntax
public ref class R {
public:
   void Finalize() {
      Console::WriteLine( "I am the R::finalizer()!" );
   }
};
```

## <a name="moving-from-managed-extensions-for-c-to-visual-c-2010"></a>Visual c + + 2010 Managed Extensions for c + + 이동

Managed Extensions for c + + 프로그램의 런타임 동작에는 참조 클래스에 trivial이 아닌 소멸자 때마다 Visual c + +에서 컴파일될 때 변경 됩니다. 필요한 변환 알고리즘은 다음과 비슷합니다.

1. 소멸자가 있는 경우 클래스 종료자로 다시 작성 하십시오.

1. 경우는 `Dispose` 메서드를 사용할 수 있는지, 클래스 소멸자로 다시 작성 합니다.

1. 소멸자는 이지만 경우 없습니다 `Dispose` 메서드를 첫 번째 항목을 수행 하는 동안 소멸자를 유지 합니다.

Managed Extensions에서 새 구문으로 코드를 이동,이 변환을 수행 하지 못할 수 있습니다. 응용 프로그램 종속 어떤 방식으로든에서 관련된 종료 메서드의 실행을 하는 경우 응용 프로그램의 동작을 자동으로 의도 한 것과에서 다릅니다.

## <a name="see-also"></a>참고 항목

[관리 되는 형식 (C + + /cli CL)](../dotnet/managed-types-cpp-cl.md)<br/>
[소멸자 및 종료자에서 방법: 클래스 및 구조체 정의 및 사용 (C + + /cli CLI)](../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers)