---
title: 컴파일러 오류 C3073 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3073
dev_langs:
- C++
helpviewer_keywords:
- C3073
ms.assetid: b24b9b8b-f9fb-4c3c-a1a0-97fad2081bfc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a46553530d8aaebaf44a71a41203764695b1868d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46050803"
---
# <a name="compiler-error-c3073"></a>컴파일러 오류 C3073

'type': ref 클래스에 사용자 정의 복사 생성자가 없습니다

에 [/clr (공용 언어 런타임 컴파일)](../../build/reference/clr-common-language-runtime-compilation.md) 컴파일, 컴파일러에서 참조 형식에 대 한 복사 생성자를 생성 하지 않습니다. 모든 **/clr** 컴파일 복사할 형식의 인스턴스로 예상 되는 경우 참조 형식에 대 한 복사 생성자를 직접 정의 해야 합니다.

자세한 내용은 [참조 형식에 대 한 c + + 스택 의미 체계](../../dotnet/cpp-stack-semantics-for-reference-types.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3073를 생성합니다.

```
// C3073.cpp
// compile with: /clr
ref class R {
public:
   R(int) {}
};

ref class S {
public:
   S(int) {}
   S(const S %rhs) {}   // copy constructor
};

void f(R) {}
void f2(S) {}
void f3(R%){}

int main() {
   R r(1);
   f(r);   // C3073
   f3(r);   // OK

   S s(1);
   f2(s);   // OK
}
```