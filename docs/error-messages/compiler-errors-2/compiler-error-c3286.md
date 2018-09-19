---
title: 컴파일러 오류 C3286 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3286
dev_langs:
- C++
helpviewer_keywords:
- C3286
ms.assetid: 554328c8-cf44-4f7d-a8d2-def74d28ecdd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9ea2a6dcccd6de6d4fc3081106123f4ab37f71a2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052916"
---
# <a name="compiler-error-c3286"></a>컴파일러 오류 C3286

> '*지정자*': 반복 변수에 저장소 클래스 지정자를 사용할 수 없습니다

저장소 클래스에 반복 변수를 지정할 수 없습니다. 자세한 내용은 참조 하세요. [저장소 클래스 (c + +)](../../cpp/storage-classes-cpp.md) 하 고 [각각의](../../dotnet/for-each-in.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3286을 생성 하 고 또한 올바른 사용법을 보여 줍니다.

```cpp
// C3286.cpp
// compile with: /clr
int main() {
   array<int> ^p = { 1, 2, 3 };
   for each (static int i in p) {}   // C3286
   for each (int j in p) {}   // OK
}
```