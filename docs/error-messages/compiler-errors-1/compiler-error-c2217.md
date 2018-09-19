---
title: 컴파일러 오류 C2217 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2217
dev_langs:
- C++
helpviewer_keywords:
- C2217
ms.assetid: 1ce1e3f5-4171-4376-804d-967f7e612935
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a4eb8b9fcaffa30f3a5ced5362a0f9d54a45f07e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46050621"
---
# <a name="compiler-error-c2217"></a>컴파일러 오류 C2217

'attribute1' 'attribute2' 필요

첫 번째 함수 특성에는 두 번째 특성에 필요합니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 중단 (`__interrupt`)로 선언 된 함수 `near`합니다. 인터럽트 함수 여야 `far`합니다.

1. 으로 선언 된 함수를 중단할 `__stdcall`, 또는 `__fastcall`합니다. 함수를 중단 해야 사용 C 호출 규칙입니다.

## <a name="example"></a>예제

C2217 가변 개수의 인수를 사용 하는 CLR 함수에 대리자를 바인딩할 경우에 발생할 수 있습니다. 함수에는 또한 e 매개 변수 배열 오버 로드에, 하는 대신 사용 합니다. 다음 샘플 C2217를 생성합니다.

```
// C2217.cpp
// compile with: /clr
using namespace System;
delegate void MyDel(String^, Object^, Object^, ...);   // C2217
delegate void MyDel2(String ^, array<Object ^> ^);   // OK

int main() {
   MyDel2^ wl = gcnew MyDel2(Console::WriteLine);
   array<Object ^ > ^ x = gcnew array<Object ^>(2);
   x[0] = safe_cast<Object^>(0);
   x[1] = safe_cast<Object^>(1);

   // wl("{0}, {1}", 0, 1);
   wl("{0}, {1}", x);
}
```