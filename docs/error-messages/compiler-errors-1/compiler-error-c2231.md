---
title: 컴파일러 오류 C2231 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2231
dev_langs:
- C++
helpviewer_keywords:
- C2231
ms.assetid: 677c5c66-d30f-4c3b-bbb9-760858d56477
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cd6cd35d20f4ce0377aa5ae5cd66cd8c08004fb8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46021682"
---
# <a name="compiler-error-c2231"></a>컴파일러 오류 C2231

'.': 왼쪽 피연산자를 가리킵니다 ' 클래스 키 ', '->' 사용

멤버 선택 연산자 (.)의 왼쪽 피연산자는 클래스, 구조체 또는 공용 구조체 대신 포인터입니다.

다음 샘플에서는 C2231을 생성합니다.

```
// C2231.c
struct S {
   int member;
} s, *ps = &s;
int main() {
   ps.member = 0;   // C2231

   // OK
   ps->member = 0;   // crash
   s.member = 0;
}
```