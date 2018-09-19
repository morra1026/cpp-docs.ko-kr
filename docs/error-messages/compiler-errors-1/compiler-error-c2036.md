---
title: 컴파일러 오류 C2036 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2036
dev_langs:
- C++
helpviewer_keywords:
- C2036
ms.assetid: 895821a9-65d1-44b5-bde1-dae827f3e486
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 105fcbaacbc35c003720cf8b1337a52e5264b26e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025349"
---
# <a name="compiler-error-c2036"></a>컴파일러 오류 C2036

'identifier': 알 수 없는 크기

에 대 한 작업 `identifier` 확인할 수 있는 데이터 개체의 크기가 필요 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2036 오류가 발생 합니다.

```
// C2036.c
// a C program
struct A* pA;
struct B { int i; } *pB;
int main() {
   pA++;   // C2036, size of A not known
   ((char*)pA)++;   // OK

   pB++;   // OK
}
```

## <a name="example"></a>예제

다음 샘플에서는 C2036 오류가 발생 합니다.

```
// C2036_2.cpp
// a C++ program
struct A* pA;
int main() {
   pA++;   // C2036, size of A not known
   ((char*&)pA)++;   // OK, if sizeof(A) == sizeof(char)
}
```