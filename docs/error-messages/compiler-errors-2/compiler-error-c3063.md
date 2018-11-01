---
title: 컴파일러 오류 C3063
ms.date: 11/04/2016
f1_keywords:
- C3063
helpviewer_keywords:
- C3063
ms.assetid: 0ecf6f1f-e4a7-487a-9fd5-79d8ac470001
ms.openlocfilehash: 9e53d9fe273a392695212df6dbeb679822a39068
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50485539"
---
# <a name="compiler-error-c3063"></a>컴파일러 오류 C3063

연산자 'operator': 모든 피연산자 열거형 형식이 있어야 합니다.

연산자에서 열거자를 사용 하는 경우 두 피연산자의 열거형 형식 이어야 합니다. 자세한 내용은 [방법: C + 열거형 정의 및 사용 + CLI](../../dotnet/how-to-define-and-consume-enums-in-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3063 생성 및이 해결 하는 방법을 보여 줍니다.

```
// C3063.cpp
// compile with: /clr
enum class E { a, b } e, mask;
int main() {
   if ( ( e & mask ) != 0 ) ;   // C3063 no operator!= (E, int)

   if ( ( e & mask ) != E() )   // OK
      ;
}
```