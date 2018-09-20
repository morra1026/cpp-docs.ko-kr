---
title: 속성 선언 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- __property keyword
- declaring properties, C++
- property keyword [C++]
ms.assetid: de169378-a8b8-49f4-a586-76bffc9b5c9f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 019b8eae17952bfe53fd8fbf14db4bafce1bf463
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46438303"
---
# <a name="property-declaration"></a>속성 선언

관리 되는 클래스의 속성을 선언 하는 방법은 Visual c + + Managed Extensions for c + + 변경 되었습니다.

Managed Extensions에서 각 디자인 `set` 또는 `get` 속성 접근자는 독자적인 방법을 활용할로 지정 됩니다. 각 메서드의 선언이 접두사로 `__property` 키워드입니다. 메서드 이름을 사용 하 여 시작 `set_` 또는 `get_` 속성 (사용자에 게 표시 됨)으로 실제 이름을 차례로 입력 합니다. 따라서를 `Vector` 제공 하는 `x` 조정 `get` 속성은 이름을 `get_x` 사용자로 호출 하 고 `x`. 이 명명 규칙 및 메서드의 별도 사양에는 실제로 속성의 기본 런타임 구현을 반영 합니다. 예를 들어, 다음은 `Vector` 좌표 속성 집합을 사용 하 여:

```
public __gc __sealed class Vector {
public:
   __property double get_x(){ return _x; }
   __property double get_y(){ return _y; }
   __property double get_z(){ return _z; }

   __property void set_x( double newx ){ _x = newx; }
   __property void set_y( double newy ){ _y = newy; }
   __property void set_z( double newz ){ _z = newz; }
};
```

이 속성을 사용 하 여 관련 기능 분산 및 연결된 집합 및 가져옵니다 어휘 적으로 통합 해야 합니다. 또한 자세한 정보 표시 됩니다. C#의 새 구문에서 `property` 키워드 뒤에 속성 이름과 해당 표시 되지 않은 형식입니다. 합니다 `set` 고 `get` 액세스 메서드 속성 이름 뒤에 나오는 블록 내에 배치 됩니다. C#과 달리 액세스 메서드 서명 지정은 참고 합니다. 예를 들어, 다음은 위의 코드 예제는 새 구문으로 변환 합니다.

```
public ref class Vector sealed {
public:
   property double x {
      double get() {
         return _x;
      }

      void set( double newx ) {
         _x = newx;
      }
   } // Note: no semi-colon
};
```

속성 액세스 메서드를 별도 액세스 수준에 같은 반영을 `public get` 와 `private` 또는 `protected set`, 명시적 액세스 레이블을 지정할 수 있습니다. 기본적으로 속성의 액세스 수준을 바깥쪽 액세스 수준에 반영 합니다. 위의 정의의 예를 들어 `Vector`모두를 `get` 하 고 `set` 메서드는 `public`합니다. 있도록를 `set` 메서드 `protected` 또는 `private`, 정의 다음과 같이 수정 됩니다.

```
public ref class Vector sealed {
public:
   property double x {
      double get() {
         return _x;
      }

   private:
      void set( double newx ) {
         _x = newx;
      }

   } // note: extent of private culminates here

// note: dot is a public method of Vector
double dot( const Vector^ wv );

// etc.
};
```

속성 내의 액세스 키워드의 범위는 속성의 닫는 중괄호 또는 추가 액세스 키워드가 지정 될 때까지 확장합니다. 속성이 정의 된 바깥쪽 액세스 수준 속성의 정의 넘어 확장 되지 않습니다. 예를 들어, 위의 선언에서 `Vector::dot()` 는 공용 메서드입니다.

세 가지에 대 한 설정 및 가져오기 속성을 쓰는 `Vector` 좌표에는 세 단계가 포함 됩니다.

1. 적절 한 유형의 전용 상태 멤버를 선언 합니다.

1. 사용자가 해당 값을 얻으려면 하고자 할 때 반환 합니다.

1. 새 값을 할당 합니다.

새 구문에서 간단한 속성 구문을 이러한 사용 패턴을 자동화 하는

```
public ref class Vector sealed {
public:
   // equivalent shorthand property syntax
   property double x;
   property double y;
   property double z;
};
```

줄임 속성 구문의 흥미로운 부수적 효과가 있다는 것 backstage 상태 멤버는 컴파일러에서 생성 되는 있지만 하지 집합/get 접근자를 통해 제외 하 고 클래스 내에서 액세스할 수 있습니다.

## <a name="see-also"></a>참고 항목

[클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)<br/>
[속성](../windows/property-cpp-component-extensions.md)