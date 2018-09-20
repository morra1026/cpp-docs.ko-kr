---
title: 대리자 및 이벤트 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- __event keyword [C++]
- delegate keyword [C++]
- delegates [C++], upgrading from Managed Extensions for C++
- __delegate keyword
- events [C++], upgrading from Managed Extensions for C++
- event keyword [C++]
ms.assetid: 3505c626-7e5f-4492-a947-0e2248f7b84a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 26b67cdce8d52cba7d02f182f0582e20d0303c33
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46373310"
---
# <a name="delegates-and-events"></a>대리자 및 이벤트

대리자 및 이벤트를 선언 하는 방법은 Visual c + + Managed Extensions for c + + 변경 되었습니다.

다음 예제와 같이 두 개의 밑줄 더 이상 필요 없는 합니다. Managed extensions에서는 샘플 코드는 다음과 같습니다.

```
__delegate void ClickEventHandler(int, double);
__delegate void DblClickEventHandler(String*);

__gc class EventSource {
   __event ClickEventHandler* OnClick;
   __event DblClickEventHandler* OnDblClick;
};
```

새 구문에서 동일한 코드를 아래와 같습니다.

```
delegate void ClickEventHandler( int, double );
delegate void DblClickEventHandler( String^ );

ref class EventSource {
   event ClickEventHandler^ OnClick;
   event DblClickEventHandler^ OnDblClick;
};
```

이벤트와 대리자는 참조 형식에는 새 구문에 분명 hat의 사용으로 인해 (`^`).  이벤트는 명시적 선언 구문을 앞 코드 에서처럼 간단한 폼을 지원 합니다. 명시적 형식에서 사용자 지정 된 `add`, `raise`, 및 `remove` 이벤트와 연결 된 메서드. (만 합니다 `add` 하 고 `remove` 방법이 필요, `raise` 메서드는 선택 사항입니다.)

Managed Extensions에서 이러한 메서드를 제공 하는 경우는 명시적 이벤트 선언도 제공 하지 않지만 존재 하지 않는 이벤트에 대 한 이름을 결정 해야 합니다. 각 메서드는 형식에서 지정 됩니다 `add_EventName`, `raise_EventName`, 및 `remove_EventName`Managed Extensions 사양에서 가져온 다음 예제 에서처럼:

```
// explicit implementations of add, remove, raise
public __delegate void f(int);
public __gc struct E {
   f* _E;
public:
   E() { _E = 0; }

   __event void add_E1(f* d) { _E += d; }

   static void Go() {
      E* pE = new E;
      pE->E1 += new f(pE, &E::handler);
      pE->E1(17);
      pE->E1 -= new f(pE, &E::handler);
      pE->E1(17);
   }

private:
   __event void raise_E1(int i) {
      if (_E)
         _E(i);
   }

protected:
   __event void remove_E1(f* d) {
      _E -= d;
   }
};
```

새 구문은 다음 변환을 보여 주듯이 선언을 간소화 합니다. 이벤트를 지정 하는 두 또는 세 개의 중괄호 쌍 안에 메서드와 같이 이벤트 및 해당 관련된 대리자 형식을 선언 바로 뒤에 배치 합니다.

```
public delegate void f( int );
public ref struct E {
private:
   f^ _E; // delegates are also reference types

public:
   E() {  // note the replacement of 0 with nullptr!
      _E = nullptr;
   }

   // the new aggregate syntax of an explicit event declaration
   event f^ E1 {
   public:
      void add( f^ d ) {
         _E += d;
      }

   protected:
      void remove( f^ d ) {
         _E -= d;
      }

   private:
      void raise( int i ) {
         if ( _E )
            _E( i );
      }
   }

   static void Go() {
      E^ pE = gcnew E;
      pE->E1 += gcnew f( pE, &E::handler );
      pE->E1( 17 );
      pE->E1 -= gcnew f( pE, &E::handler );
      pE->E1( 17 );
   }
};
```

## <a name="see-also"></a>참고 항목

[클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)<br/>
[delegate(C++ 구성 요소 확장)](../windows/delegate-cpp-component-extensions.md)<br/>
[event](../windows/event-cpp-component-extensions.md)