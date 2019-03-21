---
title: Trivial, standard-layout, POD 및 literal-type
ms.date: 04/05/2018
ms.assetid: 2b23a7be-9bad-49fc-8298-31a9a7c556b0
ms.openlocfilehash: c742f4c84a1b2ba558b790d7eea7760902da7818
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2018
ms.locfileid: "51521706"
---
# <a name="trivial-standard-layout-pod-and-literal-types"></a>Trivial, standard-layout, POD 및 literal-type

용어 *layout*은 class, struct 또는 union 형식의 멤버가 메모리에 정렬 되는 방식을 가리킵니다. 경우에 따라 layout은 언어 사양에 잘 정의 됩니다. 하지만 class 또는 struct가 virtual base class, virtual function, 접근 제어가 다른 멤버 등 특정 c++ 언어 기능을 포함하면 컴파일러는 layout을 자유롭게 선택할 수 있습니다. Layout은 수행되는 최적화에 따라 달라질 수 있으며 대부분의 경우 객체는 인접한 메모리 영역을 점유하지 않을 수도 있습니다. 예를 들어 class에 virtual function이 있는 경우 해당 class의 모든 인스턴스가 단일 virtual function table을 공유 할 수 있습니다. 물론 이러한 유형은 매우 유용하지만 한계가 있습니다. Layout이 정의되지 않았기 때문에 C와 같은 다른 언어로 작성된 프로그램에 전달할 수 없으며, 메모리가 인접하지 않을 수도 있기 때문에 memcopy와 같은 빠른 하위 수준 함수로 안정적으로 복사하거나 네트워크를 통해 직렬화 할 수 없습니다.

C++ 프로그램과 메타 프로그램뿐만 아니라 컴파일러를 사용하여 특정 메모리 레이아웃에 의존하는 작업의 특정 유형에 대한 적합성을 판단하기 위해 C++14에서는 간단한 클래스와 구조체의 세 가지 유형을 소개했습니다:*trivial*, *standard-layout*, 및 *POD* 또는 Plain Old Data. 표준 라이브러리에는 지정된 유형이 주어진 범주에 속하는지 여부를 확인하는 `is_trivial<T>`, `is_standard_layout<T>` 및 `is_pod<T>` 가 있습니다.

## <a name="trivial-types"></a>Trivial 형식

C++의 class 나 struct에 컴파일러가 제공하거나 명시적으로 특수 멤버 함수를 default로 지정하면 trivial 형식입니다. Trivial 형식은 연속적인 메모리 영역을 차지합니다. 서로 다른 접근 지정자가 있는 멤버를 가질 수 있습니다. C ++ 컴파일러는 이 상황에서 멤버 순서를 자유롭게 지정할 수 있습니다. 따라서 이러한 개체를 memcopy 할 수  있지만 C 프로그램에서 안정적으로 사용 할 수는 없습니다. Trival 타입 T는 char 또는 unsigned char의 배열에 복사 될 수 있으며 안전하게 T 변수로 다시 복사됩니다. 정렬 요구 사항 때문에 형식 멤버간에 패딩 바이트가있을 수 있습니다.

Trivial 형식은  trivial default constructor, trivial copy constructor, trivial copy assignment operator 및 trivial destructor를 가집니다. 각각의 경우에, trivial 은 constructor/operator/destructor를 사용자가 제공하지 않고 다음과 조건을 만족한다는것을 의미 합니다.

- virtual function 이나 virtual base class가 없으며,


- non-trivial constructor/operator/destructor가 있는 base class가 없습니다.


- non-trivial constructor/operator/destructor가 있는 class 유형의 데이터 멤버가 없습니다.


다음 예제는 trivial 형식을 보여줍니다. Trivial2에서 Trivial2 (int a, int b) constructor가 존재하므로 default constructor가 필요합니다. Trivial 형식으로 한정하려면 default constructor를 명시적으로 기본 설정해야합니다.

```cpp
struct Trivial
{
      int i;
private:
   int j;
   };

struct Trivial2
{
   int i;
   Trivial2(int a, int b) : i(a), j(b) {}
   Trivial2() = default;
   private:
   int j;   // Different access control
};
```

## <a name="standard-layout-types"></a>표준 레이아웃 형식

클래스 또는 구조체는 C 언어에서 제공 하지 않는 가상 함수와 같은 특정 c + + 언어 기능을 포함 하지 않으며 모든 멤버에 게 동일한 액세스 제어, 경우에 표준 레이아웃 형식입니다. Memcopy 수 이며 레이아웃 C 프로그램에서 사용할 수 있는지를 충분히 정의 됩니다. 표준 레이아웃 형식 사용자 정의 특수 멤버 함수를 사용할 수도 있습니다. 또한 표준 레이아웃 형식에 이러한 특성이 있습니다.

- 가상 함수나 가상 기본 클래스 없음

- 동일한 액세스 권한이 모든 비정적 데이터 멤버

- 클래스 형식의 모든 비정적 멤버는 표준 레이아웃

- 모든 기본 클래스는 표준 레이아웃

- 첫 번째 비정적 데이터 멤버와 동일한 형식의 기본 클래스가 없고에 있습니다.

- 이러한 조건 중 하나를 충족합니다.

  - 비정적 데이터 멤버를 사용 하 여 가장 많이 파생 된 클래스 및 둘 이상의 기본 클래스의 비정적 데이터 멤버가 없는 또는

  - 에 비정적 데이터 멤버를 사용 하 여 기본 클래스 없음

다음 코드는 표준 레이아웃 형식의 한 가지 예를 보여줍니다.

```cpp
struct SL
{
   // All members have same access:
   int i;
   int j;
   SL(int a, int b) : i(a), j(b) {} // User-defined constructor OK
};
```

마지막으로 두 가지 요구 사항이 코드로 더 설명할 아마도 있습니다. 다음 예에서 자료는 표준 레이아웃 `Derived` 아니므로 표준 레이아웃 모두 it (가장 많이 파생 된 클래스) 및 `Base` 비정적 데이터 멤버가 있는 합니다.

```cpp
struct Base
{
   int i;
   int j;
};

// std::is_standard_layout<<Derived> == false!
struct Derived : public Base
{
   int x;
   int y;
};
```

이 예제의 `Derived` 표준 레이아웃 있으므로 `Base` 비정적 데이터 멤버가 없습니다.

```cpp
struct Base
{
   void Foo() {}
};

// std::is_standard_layout<<Derived> == true
struct Derived : public Base
{
   int x;
   int y;
};
```

파생 된 표준 레이아웃도 되는 경우 `Base` 있었습니다 데이터 멤버 및 `Derived` 멤버 함수만 했습니다.

## <a name="pod-types"></a>POD 형식

클래스 또는 구조체에는 간단한 문제가 아니며 표준 레이아웃 되 면에 POD (Plain Old Data) 형식입니다. POD 형식의 메모리 레이아웃은 연속 따라서 및 각 구성원에 게 이러한 형식에서 바이트 복사 되도록 앞에 선언 된 멤버와 이진 I/O를 수행할 수 있습니다 보다 더 높은 주소입니다.  스칼라 예: int 형식은 또한 POD 형식입니다. 클래스는 POD 형식 비정적 데이터 멤버로 POD 유형만 가질 수 있습니다.

## <a name="example"></a>예제

다음 예제에서는 trivial, 표준 레이아웃 간의 차이점 및 POD 형식:

```cpp
#include <type_traits>
#include <iostream>

using namespace std;

struct B
{
protected:
   virtual void Foo() {}
};

// Neither trivial nor standard-layout
struct A : B
{
      int a;
   int b;
   void Foo() override {} // Virtual function
};

// Trivial but not standard-layout
struct C
   {
      int a;
private:
   int b;   // Different access control
};

// Standard-layout but not trivial
struct D
{
   int a;
   int b;
   D() {} //User-defined constructor
};

struct POD
{
   int a;
   int b;
};

int main()
{
   cout << boolalpha;
   cout << "A is trivial is " << is_trivial<A>() << endl; // false
   cout << "A is standard-layout is " << is_standard_layout<A>() << endl;  // false

   cout << "C is trivial is " << is_trivial<C>() << endl; // true
   cout << "C is standard-layout is " << is_standard_layout<C>() << endl;  // false

   cout << "D is trivial is " << is_trivial<D>() << endl;  // false
   cout << "D is standard-layout is " << is_standard_layout<D>() << endl; // true

   cout << "POD is trivial is " << is_trivial<POD>() << endl; // true
   cout << "POD is standard-layout is " << is_standard_layout<POD>() << endl; // true

   return 0;
}
```

## <a name="literal_types"></a> 리터럴 형식

리터럴 형식은 컴파일 타임에 해당 레이아웃이 결정될 수 있는 형식입니다. 다음은 리터럴 형식입니다.

- void
- 스칼라 형식
- 참조
- void, 스칼라 형식 또는 참조의 배열
- trivial 소멸자 및 이동 또는 복사 생성자가 아닌 constexpr 생성자를 하나 이상 포함하는 클래스입니다. 또한 해당 비정적 데이터 멤버 및 기본 클래스가 모두 리터럴 형식이고 volatile이 아니어야 합니다.

## <a name="see-also"></a>참고자료

[기본 개념](../cpp/basic-concepts-cpp.md)
