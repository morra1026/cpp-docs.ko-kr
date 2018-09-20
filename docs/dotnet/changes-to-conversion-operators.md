---
title: 변환 연산자를 변경 합니다. | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- conversion operators
- operators [C++], explicit type conversion
- type conversion, explicit conversions
- conversions, explicit
- explicit keyword [C++]
ms.assetid: 9b83925c-71b7-4bd3-ac2e-843dd7c7f184
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 03b17c5abc559289a9f85a10b9c5914b49498922
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46381116"
---
# <a name="changes-to-conversion-operators"></a>변환 연산자의 변경 내용

변환 연산자에 대 한 구문을 Visual c + + Managed Extensions for c + + 변경 되었습니다.

작성 하는 예로 `op_Implicit` 변환을 지정 합니다. 정의 같습니다. `MyDouble` 언어 사양에서 가져옵니다.

```
__gc struct MyDouble {
   static MyDouble* op_Implicit( int i );
   static int op_Explicit( MyDouble* val );
   static String* op_Explicit( MyDouble* val );
};
```

이 코드는 정수를 해당 정수로 변환 하는 알고리즘을 지정 하는 `MyDouble` 에서 제공 하는 `op_Implicit` 연산자입니다. 또한 해당 변환은 컴파일러에서 암시적으로 수행 됩니다. 마찬가지로, 지정 된 된 `MyDouble` 개체, 두 개의 `op_Explicit` 연산자는 정수 또는 관리 되는 해당 개체를 변환 하는 데 해당 알고리즘을 제공 `String` 엔터티. 그러나 컴파일러는 사용자가 명시적으로 요청 하지 않는 한 변환을 수행 하지 않습니다.

C#에서는이 모양은 다음과 같습니다.

```
class MyDouble {
   public static implicit operator MyDouble( int i );
   public static explicit operator int( MyDouble val );
   public static explicit operator string( MyDouble val );
};
```

C# 코드 Managed Extensions for c + + 보다 c + + 처럼 더 보입니다. 새 구문 에서처럼 아닙니다.

ISO-C + + 위원회 키워드 도입 `explicit`-예를 들어, 의도 하지 않은 결과 완화 하는 `Array` 차원에서는 모든 정수를 암시적으로 변환 하는 대로 단일 정수 인수를 사용 하는 클래스는 `Array` 개체는 것을 원하지 않을 경우합니다 이 문제를 방지 하는 한 가지 방법은 생성자에 더미 두 번째 인수의 디자인 방식

반면에 c + + 클래스 형식을 디자인할 때 변환 쌍을 제공 해야 합니다. 에 대 한 최상의 예는 표준 문자열 클래스입니다. 암시적 변환은 단일 인수 생성자는 C 스타일 문자열입니다. 그러나 변환 하는 문자열 C 스타일 문자열로 개체 대신 명시적으로 예제의 경우 명명 된 함수를 호출 해야 해당 암시적 변환 연산자-를 제공 하지 않습니다 `c_str()`합니다.

따라서 암시적/명시적 동작 변환 연산자 (및 캡슐화 선언의 단일 형식으로 변환 집합)에 연결 될 것 이므로 결국 합니다 변환연산자에대한원래c++지원기능이향상`explicit` 키워드입니다. C# 보다 약간 덜 자세 변환 알고리즘의 암시적 응용 프로그램을 지 원하는 연산자의 기본 동작으로 인해 변환 연산자에 대 한 Visual c + + 언어 지원은 다음과 같이 표시 됩니다.

```
ref struct MyDouble {
public:
   static operator MyDouble^ ( int i );
   static explicit operator int ( MyDouble^ val );
   static explicit operator String^ ( MyDouble^ val );
};
```

단일 인수 생성자로 선언 된 것 처럼 처리 되는 또 다른 변경 사항은 `explicit`합니다. 이 의미는 해당 호출을 트리거하기 위해 명시적 캐스트가 필요 합니다. 그러나 Note,는 명시적 변환 연산자가 정의 하 고 단일 인수 생성자 호출 됩니다.

## <a name="see-also"></a>참고 항목

[클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)