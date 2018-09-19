---
title: 컴파일러 오류 C2691 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2691
dev_langs:
- C++
helpviewer_keywords:
- C2691
ms.assetid: 6925f8f3-ea60-4909-91e6-b781492c645d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fe048537ca1d504587fe64fdd5f9b5a43af7c6e3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46100567"
---
# <a name="compiler-error-c2691"></a>컴파일러 오류 C2691

'data type': WinRTarray 또는 관리 되는이 요소 형식을 사용할 수 없습니다.

관리되는 배열 또는 WinRT 배열의 요소 형식은 값 형식이나 참조 형식일 수 있습니다.

다음 샘플에서는 C2691 오류가 발생하는 경우를 보여 줍니다.

```
// C2691a.cpp
// compile with: /clr
class A {};

int main() {
   array<A>^ a1 = gcnew array<A>(20);   // C2691
   array<int>^ a2 = gcnew array<int>(20);   // value type OK
}
```
