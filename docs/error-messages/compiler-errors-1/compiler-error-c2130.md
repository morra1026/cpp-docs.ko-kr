---
title: 컴파일러 오류 C2130
ms.date: 11/04/2016
f1_keywords:
- C2130
helpviewer_keywords:
- C2130
ms.assetid: c6fd5a7e-8f28-4f67-99d1-95a13b0dff90
ms.openlocfilehash: aee0931926cad2ac30631c152aeb94bfd24befd2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50579743"
---
# <a name="compiler-error-c2130"></a>컴파일러 오류 C2130

\#줄 필요는 파일 이름이 'token'를 포함 하는 문자열

[#line](../../preprocessor/hash-line-directive-c-cpp.md) `linenumber` 뒤에 오는 선택적 파일 이름 토큰은 문자열이어야 합니다.

다음 샘플에서는 C2130을 생성합니다.

```
// C2130.cpp
int main() {
   #line 1000 test   // C2130
   #line 1000 "test"   // OK
}
```