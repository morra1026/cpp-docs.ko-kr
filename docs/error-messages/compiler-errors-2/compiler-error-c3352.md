---
title: 컴파일러 오류 C3352
ms.date: 11/04/2016
f1_keywords:
- C3352
helpviewer_keywords:
- C3352
ms.assetid: f233bed7-474e-425f-aad2-7801578169d4
ms.openlocfilehash: c45ce5e2e72c6a987a0053cb4b1bbb151c149faf
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50496542"
---
# <a name="compiler-error-c3352"></a>컴파일러 오류 C3352

'function': 'type' 대리자 형식이 지정된 된 함수에 맞지

에 대 한 매개 변수 목록이 `function` / 대리자 일치 하지 않습니다.

자세한 내용은 [delegate (c + + 구성 요소 확장)](../../windows/delegate-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3352 오류가 생성 됩니다.

```
// C3352.cpp
// compile with: /clr
delegate int D( int, int );
ref class C {
public:
   int mf( int ) {
      return 1;
   }

   // Uncomment the following line to resolve.
   // int mf(int, int) { return 1; }
};

int main() {
   C^ pC = gcnew C;
   System::Delegate^ pD = gcnew D( pC, &C::mf );   // C3352
}
```
