---
title: 컴파일러 경고 (수준 4) C4061
ms.date: 11/30/2017
f1_keywords:
- C4061
helpviewer_keywords:
- C4061
ms.assetid: a99cf88e-7941-4519-8b1b-f6889d914b2f
ms.openlocfilehash: 8b730d561134b8b7ca4454ee74f99216fbc72cb4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50453274"
---
# <a name="compiler-warning-level-4-c4061"></a>컴파일러 경고 (수준 4) C4061

> 열거자 '*식별자*'의 switch에 '*열거형*' case 레이블에 의해 명시적으로 처리 하지 않습니다

열거자 연결된 처리기에는 `switch` 문입니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C4061; 문제를 해결 하려면 누락 된 열거자에 대 한 사례를 추가 합니다.

```cpp
// C4061.cpp
// compile with: /W4
#pragma warning(default : 4061)

enum E { a, b, c };
void func ( E e )
{
   switch(e)
   {
      case a:
      case b:
      default:
         break;
   }   // C4061 c' not handled
}

int main()
{
}
```