---
title: CLR 참조 클래스 개체 선언 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- types [C++], reference types
- reference types, CLR
ms.assetid: 6d64f746-3715-4948-ada3-88859f4150e4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: f3e8ec6407e12d0c26331d45dc1659277feed016
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46444582"
---
# <a name="declaration-of-a-clr-reference-class-object"></a>CLR 참조 클래스 개체 선언

선언 하 고 참조 클래스 형식의 개체를 인스턴스화하는 구문 Visual c + + Managed Extensions for c + + 변경 되었습니다.

Managed Extensions 참조 클래스 형식 개체의 선택적 사용을 ISO-C + + 포인터 구문을 사용 하 여 선언 되는 `__gc` 별표의 왼쪽에는 키워드 (`*`). 예를 들어 다음과 같습니다. 참조의 다양 한 관리 되는 확장 구문 클래스 형식 개체 선언

```
public __gc class Form1 : public System::Windows::Forms::Form {
private:
   System::ComponentModel::Container __gc *components;
   Button __gc *button1;
   DataGrid __gc *myDataGrid;
   DataSet __gc *myDataSet;

   void PrintValues( Array* myArr ) {
      System::Collections::IEnumerator* myEnumerator =
         myArr->GetEnumerator();

      Array *localArray;
      myArr->Copy(myArr, localArray, myArr->Length);
   }
};
```

새 구문에서 새로운 선언적 토큰을 사용 하 여 참조 클래스 형식 개체 선언 (`^`) 라고 공식적으로 *추적 핸들* 와 보다 쉽게 이야기를 *hat*합니다. (추적 형용사 참조 형식에 CLR 힙에 남아 있는 위치를 투명 하 게 가비지 컬렉션 힙 압축 하는 동안 이동 하므로 수 있음을 의미 합니다. 런타임에 대 한 추적 핸들 업데이트 투명 하 게 됩니다. 비슷한 개념을 알아야 합니다 *추적 참조* (`%`), 및 *내부 포인터* (`interior_ptr<>`)에 대 한 자세한 내용은 [값 형식 의미 체계](../dotnet/value-type-semantics.md)합니다.

선언적 구문을 ISO-C + + 포인터 구문의 재사용에서 이동 하는 주된 이유는 다음과 같습니다.

- 포인터 구문을 사용 하 여 참조 개체에 직접 적용할 오버 로드 된 연산자를 허용 하지 않았습니다. 와 같은 해당 내부 이름을 사용 하 여 연산자를 호출 해야 하나 대신 `rV1->op_Addition(rV2)` 대신 보다 직관적인 `rV1+rV2`합니다.

- 가비지에 저장 된 개체에 대해 허용 되지 캐스팅 등 포인터 산술 연산 포인터 작업 수가 수집 힙. 더 나은 추적 핸들 개념이 CLR 참조 형식의 특성을 캡처합니다.

`__gc` 추적 핸들 한정자 필요 하지 않으며 지원 되지 않습니다. 개체 자체를 사용 하 여 변경 되지 않습니다. 포인터 멤버 선택 연산자를 통해 여전히 멤버 액세스 (`->`). 예를 들어, 다음은 새 구문으로 변환 이전 Managed Extensions 코드 샘플입니다.

```
public ref class Form1: public System::Windows::Forms::Form {
private:
   System::ComponentModel::Container^ components;
   Button^ button1;
   DataGrid^ myDataGrid;
   DataSet^ myDataSet;

   void PrintValues( Array^ myArr ) {
      System::Collections::IEnumerator^ myEnumerator =
         myArr->GetEnumerator();

      Array ^localArray;
      myArr->Copy(myArr, localArray, myArr->Length);   }
};
```

## <a name="dynamic-allocation-of-an-object-on-the-clr-heap"></a>CLR 힙에 있는 개체의 동적 할당

Managed extensions, 두 개의 존재 `new` 네이티브 및 관리 되는 힙 간에 할당할 식을 대부분 투명 하 게 되었습니다. 거의 모든 인스턴스에서 컴파일러는 컨텍스트를 사용 하 여 네이티브 또는 관리 되는 힙에서 메모리를 할당할 것인지 결정할 수 있습니다. 예를 들어 개체에 적용된

```
Button *button1 = new Button; // OK: managed heap
int *pi1 = new int;           // OK: native heap
Int32 *pi2 = new Int32;       // OK: managed heap
```

상황에 맞는 힙 할당 하지 않으려면 중 하나를 사용 하 여 컴파일러에 지시할 수 있습니다 합니다 `__gc` 또는 `__nogc` 키워드입니다. 새 구문에서 두 개의 새 식의 개별 특성이 명시적으로 변경 됩니다 도입 된 `gcnew` 키워드입니다. 예를 들어, 위의 세 가지 선언은 다음과 같습니다 새 구문:

```
Button^ button1 = gcnew Button;        // OK: managed heap
int * pi1 = new int;                   // OK: native heap
Int32^ pi2 = gcnew Int32; // OK: managed heap
```

다음은 Managed Extensions 초기화는 `Form1` 이전 섹션에서 선언 된 멤버:

```
void InitializeComponent() {
   components = new System::ComponentModel::Container();
   button1 = new System::Windows::Forms::Button();
   myDataGrid = new DataGrid();

   button1->Click +=
      new System::EventHandler(this, &Form1::button1_Click);
}
```

새 구문으로 다시 캐스팅 같은 초기화는 다음과 같습니다. 대상일 경우 hat의 참조 형식에 대 한 필요 하지 않습니다는 `gcnew` 식입니다.

```
void InitializeComponent() {
   components = gcnew System::ComponentModel::Container;
   button1 = gcnew System::Windows::Forms::Button;
   myDataGrid = gcnew DataGrid;

   button1->Click +=
      gcnew System::EventHandler( this, &Form1::button1_Click );
}
```

## <a name="a-tracking-reference-to-no-object"></a>없는 개체에 대 한 추적 참조

새 구문의 `0` 더 이상 null 주소를 나타내지만 동일 정수로 처리 됩니다 `1`, `10`, 또는 `100`합니다. 새 특수 토큰에는 추적 참조에 대 한 null 값을 나타냅니다. 예를 들어, Managed Extensions에 없는 개체를 다음과 같이 해결 하기 위해 참조 형식을 초기화 합니다.

```
// OK: we set obj to refer to no object
Object * obj = 0;

// Error: no implicit boxing
Object * obj2 = 1;
```

새 구문에서 초기화 또는 할당 값의 형식에 `Object` 하면 해당 값 형식의 암시적 boxing 합니다. 새 구문에서는 둘 다 `obj` 고 `obj2` 각각 0과 1 값을 보유 하는 boxed Int32 개체의 주소를 지정할 초기화 됩니다. 예를 들어:

```
// causes the implicit boxing of both 0 and 1
Object ^ obj = 0;
Object ^ obj2 = 1;
```

따라서 명시적 초기화, 할당 및 null에 대 한 추적 핸들의 비교를 수행 하기 위해 새 키워드를 사용 하 여 `nullptr`입니다.  원래 예제를 잘못 수정 아래와 같습니다.

```
// OK: we set obj to refer to no object
Object ^ obj = nullptr;

// OK: we initialize obj2 to a Int32^
Object ^ obj2 = 1;
```

이 다소 이식 하는 기존 코드를 새 구문으로 복잡해 집니다. 예를 들어, 다음 값 클래스 선언을 고려 하십시오.

```
__value struct Holder {
   Holder( Continuation* c, Sexpr* v ) {
      cont = c;
      value = v;
      args = 0;
      env = 0;
   }

private:
   Continuation* cont;
   Sexpr * value;
   Environment* env;
   Sexpr * args __gc [];
};
```

여기에서는 둘 다 `args` 및 `env` 는 CLR 참조 형식입니다. 이러한 두 멤버를 초기화 `0` 생성자에서 그대로 유지 되지 새 구문으로 전환 합니다. 하도록 변경 되어야 합니다 아니라 `nullptr`:

```
value struct Holder {
   Holder( Continuation^ c, Sexpr^ v )
   {
      cont = c;
      value = v;
      args = nullptr;
      env = nullptr;
   }

private:
   Continuation^ cont;
   Sexpr^ value;
   Environment^ env;
   array<Sexpr^>^ args;
};
```

마찬가지로, 비교 하도록 해당 멤버에 대 한 테스트 `0` 멤버를 비교 하려면 변경 해야 `nullptr`합니다. Managed Extensions 구문은 다음과 같습니다.

```
Sexpr * Loop (Sexpr* input) {
   value = 0;
   Holder holder = Interpret(this, input, env);

   while (holder.cont != 0) {
      if (holder.env != 0) {
         holder=Interpret(holder.cont,holder.value,holder.env);
      }
      else if (holder.args != 0) {
         holder =
         holder.value->closure()->
         apply(holder.cont,holder.args);
      }
   }

   return value;
}
```

각 교체 수정 버전을 다음과 같습니다 `0` 인스턴스는 `nullptr`합니다. 대부분을 자동화 하 여이 변환에서 변환 도구를 통해 그렇지 않은 경우 모든 항목을 포함 하 여 사용 된 `NULL` 매크로입니다.

```
Sexpr ^ Loop (Sexpr^ input) {
   value = nullptr;
   Holder holder = Interpret(this, input, env);

   while ( holder.cont != nullptr ) {
      if ( holder.env != nullptr ) {
         holder=Interpret(holder.cont,holder.value,holder.env);
      }
      else if (holder.args != nullptr ) {
         holder =
         holder.value->closure()->
         apply(holder.cont,holder.args);
      }
   }

   return value;
}
```

`nullptr` 는 포인터나 추적 핸들 형식으로 변환 되지만 정수 계열 형식으로 승격 되지 않습니다. 다음 집합이 초기화의 예를 들어를 `nullptr` 를 초기 값 으로만 유효 합니다.

```
// OK: we set obj and pstr to refer to no object
Object^ obj = nullptr;
char*   pstr = nullptr; // 0 would also work here

// Error: no conversion of nullptr to 0
int ival = nullptr;
```

마찬가지로, 다음과 같은 메서드의 오버 로드 된 집합을 지정:

```
void f( Object^ ); // (1)
void f( char* );   // (2)
void f( int );     // (3)
```

사용 하 여 호출 `nullptr` 다음과 같은 리터럴

```
// Error: ambiguous: matches (1) and (2)
f(  nullptr );
```

모호 하기 때문에 `nullptr` 추적 핸들 및 포인터를 둘 다 일치 하 다른 됩니다 및 합니다. (이 경우 명시적 캐스트가 필요 명확 하 게 하기 위해.)

사용 하 여 호출 `0` 정확히 일치 인스턴스 (3):

```
// OK: matches (3)
f( 0 );
```

때문에 `0` 는 정수 형식입니다. 되었습니다 `f(int)` 없는 호출 명확 하 게 일치 `f(char*)` 표준 변환을 통해. 일치 규칙 표준 변환을 통한 일치 우선 순위를 제공합니다. 정확히 일치 하는 없을 경우에서 표준 변환은 보다 우선을 순위가 높습니다 값 형식의 암시적 boxing 합니다. 모호성이 없는 이유입니다.

## <a name="see-also"></a>참고 항목

[관리 되는 형식 (C + + /cli CL)](../dotnet/managed-types-cpp-cl.md)<br/>
[클래스 및 구조체](../windows/classes-and-structs-cpp-component-extensions.md)<br/>
[개체 연산자 (^)에 대 한 핸들](../windows/handle-to-object-operator-hat-cpp-component-extensions.md)<br/>
[nullptr](../windows/nullptr-cpp-component-extensions.md)