---
title: 값 형식 명시적 Boxing | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- boxing, Visual C++
- __box keyword
- boxing
- boxing, __box keyword
- value types, boxed
ms.assetid: 9597c92f-a3fe-44af-ad80-f9d656847a35
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: e9c232dba6d766d0855bb4bb29e33d85b5fd5a2d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46387590"
---
# <a name="implicit-boxing-of-value-types"></a>값 형식 명시적 boxing

값 형식의 boxing Visual c + + Managed Extensions for c + + 변경 되었습니다.

언어 설계에 기능을 사용 하 여 실제 경험 하는 대신 철학적 위치를 적용 했습니다 했으며, 실제로 실수입니다. 예를 들어,으로 원래에서 여러 상속 언어 디자인, Stroustrup 결정 파생된 클래스 생성자 내에서 가상 기본 클래스가 하위 개체를 초기화할 수 없습니다 하 고 따라서 언어 필요 하는 가상 기본으로 제공 하는 모든 클래스 클래스는 기본 생성자를 정의 해야 합니다. 이후의 모든 가상 파생 하 여 호출 되는 기본 생성자는 것입니다.

가상 기본 클래스 계층의 각 후속 파생을 사용 하 여 가상 공유 하위 개체의 초기화에 대 한 책임 이동는입니다. 예를 들어, 기본 클래스를 정의 하는 경우 초기화 버퍼는 버퍼의 사용자 지정 크기 할당이 필요한 수 수 인수로 서 생성자에 전달 합니다. 다음 두 개의 가상 파생 제공, 부르 `inputb` 및 `outputb`, 각 기본 클래스 생성자에는 특정 값을 제공 합니다. 이제 파생을 `in_out` 둘 다에서 클래스 `inputb` 및 `outputb`, 계산 될 수 있는 공유 가상 기본 클래스가 하위 개체에 해당 값을 모두 합니다.

따라서 원래 언어 디자인에서 Stroustrup 가상 기본 클래스의 멤버가 초기화 목록 내의 파생된 클래스 생성자를 명시적으로 초기화할 수 없습니다. 문제 해결이 있지만 실제로 가상 기본 클래스의 초기화를 직접 수 없다는 점을 입증 impracticable 합니다. National Institute의 상태, Keith Gorlen 했습니다 nihcl 이라는 SmallTalk 컬렉션 라이브러리의 프리웨어 버전을 구현 하는 그 보다 유연한 언어 디자인을 수립 해야 했던 Stroustrup 유도에서 원칙 음성 했습니다.

개체 지향 계층 구조 디자인의 원리는 파생된 클래스 관련 되어야 해당 직접 기본 클래스의 private이 아닌 구현과 보유 합니다. 가상 상속에 대 한 유연한 초기화 디자인을 지원 하기 위해 Stroustrup이이 원칙을 위반 했습니다. 계층 구조에서 가장 많이 파생 된 클래스 계층 구조의에 얼마나 깊이 관계 없이 모든 가상 하위 개체 초기화에 대 한 책임을 가정 합니다. 예를 들어 `inputb` 고 `outputb` 둘 다 명시적으로 즉시 가상 기본 클래스를 초기화 하는 일을 담당 합니다. 때 `in_out` 모두에서 파생 되 `inputb` 하 고 `outputb`를 `in_out` 를 한 번의 초기화를 가상 기본 클래스를 제거 하 고 내에서 명시적 초기화 수행에 대 한 책임을 집니다 `inputb` 및 `outputb` 는 표시 되지 않습니다.

이 언어 개발자가 있지만 의미가 복잡해 지는 데 필요한 유연성을 제공 합니다. 가상 기본 클래스를 상태 없이 단순히 인터페이스를 지정할 수 있도록 제한 하면 complication의 이러한 부담 제거 됩니다. C + + 내에서 권장 되는 디자인 방식입니다. Clr 프로그래밍, 인터페이스 형식 사용 하 여 정책에 발생 합니다.

다음은 간단한 코드 샘플-및 명시적 boxing 필요 없는 예제의 경우:

```
// Managed Extensions for C++ requires explicit __box operation
int my1DIntArray __gc[] = { 1, 2, 3, 4, 5 };
Object* myObjArray __gc[] = {
   __box(26), __box(27), __box(28), __box(29), __box(30)
};

Console::WriteLine( "{0}\t{1}\t{2}", __box(0),
   __box(my1DIntArray->GetLowerBound(0)),
   __box(my1DIntArray->GetUpperBound(0)) );
```

알 수 있듯이 진행 되는 boxing 많은 방법이 있습니다. Visual c + +, 값 형식이 boxing은 암시적:

```
// new syntax makes boxing implicit
array<int>^ my1DIntArray = {1,2,3,4,5};
array<Object^>^ myObjArray = {26,27,28,29,30};

Console::WriteLine( "{0}\t{1}\t{2}", 0,
   my1DIntArray->GetLowerBound( 0 ),
   my1DIntArray->GetUpperBound( 0 ) );
```

## <a name="see-also"></a>참고 항목

[값 형식 및 동작(C++/CLI)](../dotnet/value-types-and-their-behaviors-cpp-cli.md)<br/>
[Boxing](../windows/boxing-cpp-component-extensions.md)