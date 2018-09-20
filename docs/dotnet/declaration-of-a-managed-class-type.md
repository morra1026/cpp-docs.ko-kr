---
title: 관리 되는 클래스 형식 선언의 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- __gc types
- classes [C++], managed
- class keyword [C++], CLR
- __value keyword
- value types, declaring
- value keyword [C++]
- managed classes
- interface class keyword
- ref keyword [C++]
ms.assetid: 16de9c94-91d7-492f-8ac7-f0729cc627e9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 0f9ceb0867fbdfbbdb46075662fca802d1ee0bba
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46393674"
---
# <a name="declaration-of-a-managed-class-type"></a>관리되는 클래스 형식 선언

Visual c + +에서 Managed Extensions for c + + 변경 참조 클래스 형식을 선언 하는 방법입니다.

Managed Extensions에서 참조 클래스 형식 앞에 사용 된 `__gc` 키워드입니다. 새 구문에는 `__gc` 키워드는 두 개의 공백이 포함 된 키워드 중 하나에 의해 바뀝니다: `ref class` 또는 `ref struct`합니다. 선택할 `struct` 또는 `class` 공용 나타냅니다 (에 대 한 `struct`) 또는 개인 (에 대 한 `class`) 형식의 본문의 초기 레이블이 지정 되지 않은 섹션에서 선언 된 해당 멤버의 기본 액세스 수준입니다.

마찬가지로, Managed extensions에서 값 클래스 형식 앞의 `__value` 키워드입니다. 새 구문에는 `__value` 키워드는 두 개의 공백이 포함 된 키워드 중 하나에 의해 바뀝니다: `value class` 또는 `value struct`합니다.

Managed extensions에서 인터페이스 형식, 키워드를 사용 하 여 지정 된 `__interface`합니다. 새 구문에서이 바뀝니다 `interface class`합니다.

예를 들어, 다음 클래스 선언은 Managed Extensions에서:

```
public __gc class Block {};     // reference class
public __value class Vector {}; // value class
public __interface IFooBar {};  // interface class
```

새 구문에서이 동등 하 게 같이 선언 됩니다.

```
public ref class Block {};         // reference class
public value class Vector {};      // value class
public interface class IFooBar {}; // interface class
```

## <a name="specifying-the-class-as-abstract"></a>클래스를 추상으로 지정

키워드를 입력 하면 Managed extensions `__abstract` 하기 전에 `class` 키워드 (전후는 `__gc`)를 클래스 완료 되었음을 나타내고 프로그램 내에서 클래스의 개체를 만들 수 없습니다:

```
public __gc __abstract class Shape {};
public __gc __abstract class Shape2D: public Shape {};
```

새 구문에서 지정 하는 `abstract` 클래스 이름 및 클래스 본문, 기본 클래스 파생 목록 또는 세미콜론 앞 다음 상황별 키워드입니다.

```
public ref class Shape abstract {};
public ref class Shape2D abstract : public Shape{};
```

물론, 의미 체계 의미는 변경 되지 않습니다.

## <a name="specifying-the-class-as-sealed"></a>봉인 된 대로 클래스를 지정 합니다.

키워드를 입력 하면 Managed extensions `__sealed` 하기 전에 `class` 키워드 (전후 `__gc`)에서 클래스의 개체를 상속할 수 없습니다를 나타내기 위해:

```
public __gc __sealed class String {};
```

새 구문에서 지정 하는 `sealed` 클래스 이름 및 클래스 본문, 기본 클래스 파생 목록 또는 세미콜론 앞 다음 상황별 키워드입니다.

클래스를 파생와 봉인할 수 있습니다. 예를 들어 합니다 `String` 에서 암시적으로 파생 된 클래스 `Object`합니다. 봉인 클래스의 장점은 정적 해상도 지원 하는지 (즉, 컴파일 시간에) sealed 참조 클래스 개체를 통해 모든 가상 함수 호출 합니다. 왜냐하면 합니다 `sealed` 지정자를 사용 하면를 `String` 호출 되는 가상 메서드의 재정의 인스턴스를 제공할 수 있는 한 이후에 파생된 클래스를 참조할 수 추적 핸들입니다. 새 구문에서 봉인 된 클래스의 예는 다음과 같습니다.

```
public ref class String sealed {};
```

클래스 모두 추상으로도 지정할 수 있습니다 이며 sealed-이 정적 클래스를 지정 하는 특별 한 상태입니다. 다음과 같이 CLR 설명서에 설명 되어이 있습니다.

"는 모두 즉 입력할 `abstract` 고 `sealed` 정적 멤버가 있어야 하며 역할 무엇을 일부 언어 네임 스페이스를 호출 해야 합니다."

예를 들어 다음과 같습니다. 관리 되는 확장 구문을 사용 하 여 봉인 된 추상 클래스의 선언

```
public __gc __sealed __abstract class State {
public:
   static State() {}
   static bool inParamList();

private:
   static bool ms_inParam;
};
```

및 새 구문으로 변환 하는이 선언은 다음과 같습니다.

```
public ref class State abstract sealed {
public:
   static State();
   static bool inParamList();

private:
   static bool ms_inParam;
};
```

## <a name="clr-inheritance-specifying-the-base-class"></a>기본 클래스를 지정 하는 CLR 상속:

CLR 개체 모델에서 공용 단일 상속만 지원 됩니다. 그러나 Managed Extensions 보존 개인 파생을 지정 하는 것을 액세스 키워드 없이 기본 클래스의 ISO-C + + 기본 해석입니다. 즉, 각 CLR 상속 선언을 제공 해야 하는 `public` 기본 해석을 재정의 하는 키워드입니다.

```
// Managed Extensions: error: defaults to private derivation
__gc class Derived : Base {};
```

새 구문 정의 액세스 키워드가 없는 경우 CLR 상속 정의에 공용 파생을 나타냅니다. 따라서는 `public` 액세스 키워드는 이제 선택적 요소입니다. C + + 코드에 대 한 Managed Extensions의 수정할 필요가 없습니다, 하는 동안 완전성을 위해이 변경 여기 나열 합니다.

```
// New syntax: ok: defaults to public derivation
ref class Derived : Base{};
```

## <a name="see-also"></a>참고 항목

[관리 되는 형식 (C + + /cli CL)](../dotnet/managed-types-cpp-cl.md)<br/>
[클래스 및 구조체](../windows/classes-and-structs-cpp-component-extensions.md)<br/>
[abstract](../windows/abstract-cpp-component-extensions.md)<br/>
[sealed](../windows/sealed-cpp-component-extensions.md)