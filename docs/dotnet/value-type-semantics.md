---
title: 값 형식 의미 체계 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- interior_ptr keyword [C++]
- virtual functions, value types
- inheritance, value types
- pinning pointers
- pin_ptr keyword [C++]
- __pin keyword
ms.assetid: 7f065589-ad25-4850-baf1-985142e35e52
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 72dc6a613616d13e9ff92e8af0c39c63dfe63162
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413798"
---
# <a name="value-type-semantics"></a>값 형식 의미

값 형식 의미 체계 Visual c + + Managed Extensions for c + + 변경 되었습니다.

다음은 c + + 사양에 대 한 Managed Extensions에 사용 된 정식 간단한 값 형식입니다.

```
__value struct V { int i; };
__gc struct R { V vr; };
```

Managed Extensions (위치 2 및 3 양식은 동일한 의미 체계가) 값 형식의 네 가지 구문 변형이 있을 수 있습니다 것:

```
V v = { 0 };       // Form (1)
V *pv = 0;         // Form (2) an implicit form of (3)
V __gc *pvgc = 0;  // Form (3)
__box V* pvbx = 0; // Form (4) must be local
```

## <a name="invoking-inherited-virtual-methods"></a>상속 된 가상 메서드를 호출합니다.

`Form (1)` 정식 값 개체 이며 비교적 잘 알려져와 같은 상속 된 가상 메서드를 호출 하려고 할 때 사용자가 제외 하 고 `ToString()`입니다. 예를 들어:

```
v.ToString(); // error!
```

재정의 하지 않으므로이 메서드를 호출 하기 위해 `V`, 컴파일러는 기본 클래스의 관련된 가상 테이블에 액세스할 수 있어야 합니다. 값 형식은 해당 가상 테이블 (vptr)에 연결 된 포인터 저장소에서 상태 이기 때문에이 실행 하려면 `v` 넣을 합니다. Managed Extensions 언어 디자인에서는 암시적 boxing은 지원 되지 않지만 에서처럼 프로그래머가 명시적 지정 되어야 합니다.

```
__box( v )->ToString(); // Managed Extensions: note the arrow
```

이러한 설계의 기본 동기는 사용해: 메커니즘을 기본 그녀 '원가' 자신의 값 형식 내에서 인스턴스를 제공 하지 않는 이해할 수 있도록 프로그래머에 게 표시 되도록 해야 합니다. 되었습니다 `V` 의 인스턴스를 포함 하도록 `ToString`, boxing 필요 하지 않을 것입니다.

하지만 자체 boxing 하지 기본 비용을 명시적으로 boxing의 어휘 복잡성 새 구문에서 제거 됩니다.

```
v.ToString(); // new syntax
```

클래스 디자이너의 명시적 인스턴스를 제공 하지 않는 데의 비용에 대 한 잘못 된 수 있지만 합니다 `ToString` 메서드 내에서 `V`합니다. 암시적 boxing 원인은 일반적으로 하나의 클래스 디자이너는 사용자가 자유롭게 수정할 수 있는 누구도 무제한 `V` 가능한 성가실 명시적 상자를 제거 하려면.

재정의 인스턴스 제공 여부를 결정 하는 조건을 `ToString` 값 내에서 클래스 빈도 해당 사용 위치 여야 합니다. 거의 호출 될 경우 물론 해당 정의에 따른 이점이 거의 합니다. 마찬가지로, 응용 프로그램의 효율적이 지 않은 영역을 호출 하는 경우 추가 해 서 추가 응용 프로그램의 전반적인 성능이 합니다. 또는 boxed 값에 대 한 추적 핸들 유지할 수 있습니다 하 고 해당 핸들을 통해 호출 boxing 필요 하지 않습니다.

## <a name="there-is-no-longer-a-value-class-default-constructor"></a>값 클래스 기본 생성자가 더 이상

또 다른 차이점 값 형식 사용 하 여 관리 되는 확장 및 새로운 구문을 기본 생성자에 대 한 지원 제거 하는 것입니다. 연결 된 기본 생성자를 호출 하지 않고 CLR 값 형식의 인스턴스를 만들 수는 실행 하는 동안 경우가 있기 때문입니다. 즉, 값 형식 내에서 기본 생성자를 지원 하기 위해 Managed extensions 시도 수 있습니다. 하지 연습 보장할 수 있습니다. 보장이 지정 되 면 해당 것으로 판단 되었으므로 해당 응용 프로그램에서 명확 하 게 하는 것이 아니라 지원을 완전히 삭제 하는 것이 좋습니다.

이 결과 생각 만큼 나쁘지 않습니다. 값 형식의 각 개체는 자동으로 없어지는 이므로 (유형별로 해당 기본값으로 초기화 됩니다.). 결과적으로, 로컬 인스턴스 멤버는 정의 되지 않습니다. 이런 점에서 trivial 기본 생성자를 정의 하는 기능 손실 실제로 손실 전혀-아니며이 실제로 CLR에서 수행 하는 경우에 더 효율적입니다.

Managed Extensions의 사용자는 trivial이 아닌 기본 생성자를 정의 하는 경우이 문제가입니다. 이 새 구문에 대 한 매핑이 없습니다. 생성자 내에서 코드를 다음 사용자가 명시적으로 호출 해야 하는 명명 된 초기화 메서드를 마이그레이션해야 할 수 있습니다.

그렇지 않으면 새 구문 내에서 값 형식 개체의 선언을 변경 되지 않습니다. 이 아래쪽 변의 값 형식이 아니라는 네이티브 형식의 줄 바꿈에 대해 만족 스 럽 지 다음과 같은 이유로:

- 값 형식에서 소멸자에 대 한 지원은 없습니다. 즉, 일련의 개체의 수명 끝에 의해 트리거되는 작업을 자동화할 수 없는 방법이 있습니다.

- 다음 네이티브 힙에 할당 되는 포인터와 관리 되는 형식 내 에서만 네이티브 클래스를 포함할 수 있습니다.

값 형식이 참조 형식이 아니라 이중 힙 할당을 방지 하기에 작은 네이티브 클래스 래핑 하고자 합니다: 기본 종류를 보유 하는 네이티브 힙 및 관리 되는 래퍼를 저장 하는 CLR 힙. 값 형식 내에서 네이티브 클래스 래핑 하는 관리 되는 힙에 방지할 수 있습니다 하지만 네이티브 힙 메모리의 재사용을 자동화할 수 없습니다를 제공 합니다. 참조 형식은 trivial이 아닌 기본 클래스를 래핑하는 관리 되는 유일한 형식입니다.

## <a name="interior-pointers"></a>내부 포인터

`Form (2)` 및 `Form (3)` 위에 해결할 수 있습니다 (즉, 모든 관리 되는 또는 네이티브) 다음이이 환경에 거의 모든 합니다. 따라서 예를 들어 Managed Extensions에서 다음 작업을 모두 허용 됩니다.

```
__value struct V { int i; };
__gc struct R { V vr; };

V v = { 0 };  // Form (1)
V *pv = 0;  // Form (2)
V __gc *pvgc = 0;  // Form (3)
__box V* pvbx = 0;  // Form (4)

R* r;

pv = &v;            // address a value type on the stack
pv = __nogc new V;  // address a value type on native heap
pv = pvgc;          // we are not sure what this addresses
pv = pvbx;          // address a boxed value type on managed heap
pv = &r->vr;        // an interior pointer to value type within a
                    //    reference type on the managed heap
```

따라서는 `V*` 로컬 블록 내에서 위치를 해결할 수 있습니다 (및 따라서 수 현 수 참조일 수), 네이티브 내에서 전역 범위에서 CLR 힙 내에서 (예를 들어 주소 개체가 이미 삭제 된 경우), 힙 (및 따라서을 추적 해야 하는 경우 옮겨야 하는 동안 가비지 수집), (내부 포인터를이 호출할 때 투명 하 게도 추적 됩니다) CLR 힙에 대 한 참조 개체의 내부 내에서.

Managed extensions에서는의 기본 측면을 분리할 수 없습니다는 `V*`; 즉, 처리는 포괄적인 측면에서 개체 또는 관리 되는 힙에 대 한 하위 개체의 가능성을 처리 하는 합니다.

새 구문에서는 값 형식 포인터 두 가지 유형으로 구분 됩니다. `V*`, 비-CLR 힙 위치 및 내부 포인터로 제한 되는 `interior_ptr<V>`는 허용 하지만 관리 되는 힙 내의 주소 필요 하지 않습니다.

```
// may not address within managed heap
V *pv = 0;

// may or may not address within managed heap
interior_ptr<V> pvgc = nullptr;
```

`Form (2)` 및 `Form (3)` Managed extensions를 매핑할 `interior_ptr<V>`합니다. `Form (4)` 추적 핸들이입니다. 관리 되는 힙 내의 boxed는 전체 개체를 주소를 지정 합니다. 새 구문으로 변환 되는 `V^`,

```
V^ pvbx = nullptr; // __box V* pvbx = 0;
```

모든 새 구문에서는 내부 포인터에 대 한 지도 Managed Extensions의 다음 선언 합니다. (값 형식 내에서 `System` 네임 스페이스입니다.)

```
Int32 *pi;   // => interior_ptr<Int32> pi;
Boolean *pb; // => interior_ptr<Boolean> pb;
E *pe;       // => interior_ptr<E> pe; // Enumeration
```

기본 제공 형식은 관리 되는 형식 라고 내의 형식에 대 한 별칭으로 사용 되더라도 `System` 네임 스페이스입니다. 따라서 다음 매핑이 유효 Managed Extensions 사이의 새 구문:

```
int * pi;     // => int* pi;
int __gc * pi2; // => interior_ptr<int> pi2;
```

변환 하는 경우는 `V*` 가장 보수적인 전략은 기존 프로그램에 항상로 설정 하는 `interior_ptr<V>`합니다. Managed Extensions에서 처리 된 방법입니다. 새 구문에서 프로그래머는 관리 되지 않는 힙 주소 지정 하 여 값 형식을 제한할 `V*` 내부 포인터를 대신 합니다. 프로그램을 변환할 때 모든 사용의 전이적 closure를 수행할 수 있고 관리 되는 힙에 할당 된 주소가 인지, 하는 경우 남겨 두는 것으로 `V*` 괜찮습니다.

## <a name="pinning-pointers"></a>포인터 고정

가비지 수집기는 압축 단계 일반적으로 힙 내의 다른 위치로 CLR 힙에 있는 개체를 이동할 필요에 따라 수 있습니다. 이 이동 핸들, 추적 참조 및 이러한 엔터티를 투명 하 게 업데이트 하는 내부 포인터를 추적 하는 문제가 되지 않습니다. 그러나이 이동을 문제가 있는 경우, 사용자는 런타임 환경 외부에서 CLR 힙에 개체의 주소 경과한 경우 이 예제의 volatile 이동 개체의 경우 런타임 오류가 발생할 수 있습니다. 이동, 외부 사용의 범위에 대 한 해당 위치에 로컬로 고정 해야 것 같은 예외 개체입니다.

Managed extensions에서는 *고정 포인터* 사용 하는 포인터 선언이 정규화 하 여 선언 된는 `__pin` 키워드입니다. Managed Extensions 사양에서 약간 수정 하는 예제는 다음과 같습니다.

```
__gc struct H { int j; };

int main()
{
   H * h = new H;
   int __pin * k = & h -> j;

   // ...
};
```

새 언어 디자인, 내부 포인터의 유사 구문을 사용 하 여 고정 포인터를 선언 합니다.

```
ref struct H
{
public:
   int j;
};

int main()
{
   H^ h = gcnew H;
   pin_ptr<int> k = &h->j;

   // ...
}
```

새 구문에 대 한 고정 포인터는 내부 포인터의 특수 사례입니다. 고정 포인터에 대 한 원래 제약 조건이 남아 있습니다. 예를 들어, 매개 변수로 사용할 수 없습니다 또는; 메서드의 형식을 반환 합니다. 로컬 개체에 대해서만 선언할 수 있습니다. 그러나 새 구문에 추가 되었습니다 다양 한 제약 조건 추가 합니다.

고정 포인터의 기본값은 `nullptr`이 아니라 `0`합니다. A `pin_ptr<>` 초기화 하거나 할당할 수 없습니다. `0`합니다. 모든 할당이 `0` 기존 코드 해야 하도록 변경 `nullptr`합니다.

Managed Extensions에서 고정 포인터는 Managed Extensions 사양에서 가져온 다음 예제와 같이 전체 개체를 해결 하기 위해 허용 되었습니다.

```
__gc class G {
public:
   void incr(int* pi) { pi += 1; }
};
__gc struct H { int j; };
void f( G * g ) {
   H __pin * pH = new H;
   g->incr(& pH -> j);
};
```

새 구문에는 전체 개체를 고정 반환한는 `new` 식은 지원 되지 않습니다. 대신, 내부 멤버의 주소를 고정 해야 합니다. 예를 들어 개체에 적용된

```
ref class G {
public:
   void incr(int* pi) { *pi += 1; }
};
ref struct H { int j; };
void f( G^ g ) {
   H ^ph = gcnew H;
   Console::WriteLine(ph->j);
   pin_ptr<int> pj = &ph->j;
   g->incr(  pj );
   Console::WriteLine(ph->j);
}
```

## <a name="see-also"></a>참고 항목

[값 형식 및 동작(C++/CLI)](../dotnet/value-types-and-their-behaviors-cpp-cli.md)<br/>
[클래스 및 구조체](../windows/classes-and-structs-cpp-component-extensions.md)<br/>
[interior_ptr(C++/CLI)](../windows/interior-ptr-cpp-cli.md)<br/>
[pin_ptr(C++/CLI)](../windows/pin-ptr-cpp-cli.md)