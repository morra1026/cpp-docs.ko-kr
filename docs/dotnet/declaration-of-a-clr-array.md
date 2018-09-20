---
title: CLR 배열 선언 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- array keyword [C++]
ms.assetid: 36a8883c-2663-43f0-a90c-28f27035e036
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: c3de17bb293e10c4e1a2287ef12b934633b1fe21
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46426460"
---
# <a name="declaration-of-a-clr-array"></a>CLR 배열 선언

선언에 대 한 구문, 인스턴스화 및 관리 되는 배열을 초기화로 변경 되었습니다 Managed Extensions에서 c + + 용 Visual c + +.

Managed Extensions에서 CLR 배열 개체의 선언 된는 표준 배열 선언의 확장을 `__gc` 배열 개체의 이름 및 해당 쉼표로 채워진 차원 같이 다음 한 쌍 사이 키워드 배치 된 예제:

```
void PrintValues( Object* myArr __gc[]);
void PrintValues( int myArr __gc[,,]);
```

이 템플릿-비슷한 선언을 c + + 표준 라이브러리는 사용 하는, 새 구문에서 간단해졌습니다 `vector` 선언 합니다. 첫 번째 매개 변수 요소 형식을 나타냅니다. 두 번째 매개 변수는 배열 차원 지정 (기본값은 1 사용 하 여 여러 차원 으로만 필요 두 번째 인수). 배열 개체 자체 추적 핸들 및 따라서 해야 캐럿을 사용 합니다. 요소 형식이 참조 형식이 인 경우에 hat도 필요 합니다. 예를 들어 위의 예제에서는 새 구문으로 표현 하면 다음과 같이 표시 됩니다.

```
void PrintValues( array<Object^>^ myArr );
void PrintValues( array<int,3>^ myArr );
```

참조 형식 개체를 사용 하지 않고 추적 핸들 이므로 CLR 배열 함수의 반환 형식으로 지정할 수는 있습니다. (반대로 수 없는 네이티브 배열은 함수의 반환 형식으로 지정 합니다.) Managed Extensions에서이 작업을 수행 하는 구문은 약간 직관적이 지 않은 경우 예를 들어:

```
Int32 f() [];
int GetArray() __gc[];
```

Visual c + +에서 선언 훨씬 쉽습니다. 예를 들어 개체에 적용된

```
array<Int32>^ f();
array<int>^ GetArray();
```

로컬 관리 되는 배열의 줄임 초기화는 언어의 버전 모두에서 지원 됩니다. 예를 들어:

```
int GetArray() __gc[] {
   int a1 __gc[] = { 1, 2, 3, 4, 5 };
   Object* myObjArray __gc[] = {
      __box(26), __box(27), __box(28), __box(29), __box(30)
   };
   return a1;
}
```

새 구문에서는 상당히 간단 (boxing은 새 구문에서 암시적 되므로 합니다 `__box` 연산자가 제거 되어-참조 [값 형식 및 해당 동작 (C + + /cli CLI)](../dotnet/value-types-and-their-behaviors-cpp-cli.md) 토론에 대 한):

```
array<int>^ GetArray() {
   array<int>^ a1 = {1,2,3,4,5};
   array<Object^>^ myObjArray = {26,27,28,29,30};
   return a1;
}
```

배열 CLR 참조 형식 이므로 각 배열 개체의 선언을 추적 핸들입니다. 따라서 CLR 힙에 배열 개체를 할당 해야 합니다. (인쇄 줄임 표기 관리 되는 힙 할당을 숨깁니다.) 명시적 형식의 Managed extensions 배열 개체 초기화는 다음과 같습니다.

```
Object* myArray[] = new Object*[2];
String* myMat[,] = new String*[4,4];
```

새 구문에서는 합니다 `new` 식으로 대체 됩니다 `gcnew`합니다. 차원 크기를 매개 변수로 전달 되는 `gcnew` 같이 식:

```
array<Object^>^ myArray = gcnew array<Object^>(2);
array<String^,2>^ myMat = gcnew array<String^,2>(4,4);
```

새 구문에는 명시적 초기화 목록을 따르면는 `gcnew` 식;이 된 Managed Extensions에서 지원 되지 않습니다. 예를 들어:

```
// explicit initialization list following gcnew
// was not supported in Managed Extensions
array<Object^>^ myArray =
   gcnew array<Object^>(4){ 1, 1, 2, 3 };
```

## <a name="see-also"></a>참고 항목

[관리 되는 형식 (C + + /cli CL)](../dotnet/managed-types-cpp-cl.md)<br/>
[배열](../windows/arrays-cpp-component-extensions.md)