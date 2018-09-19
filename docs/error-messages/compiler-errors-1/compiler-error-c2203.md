---
title: 컴파일러 오류 C2203 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2203
dev_langs:
- C++
helpviewer_keywords:
- C2203
ms.assetid: 5497df43-86f6-43d5-b6cb-723c4c589b10
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6db497a7967e0cefc16ecb6e5a71874f86179b29
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053767"
---
# <a name="compiler-error-c2203"></a>컴파일러 오류 C2203

삭제 연산자는 배열의 범위를 지정할 수 없습니다

사용 하 여를 **/Za** (ANSI) 옵션을 `delete` 운영자 파트 또는 배열의 특정 멤버 안 배열 전체를 삭제할 수 있습니다.

다음 샘플에서는 C2203 오류가 생성 됩니다.

```
// C2203.cpp
// compile with: /Za
int main() {
   int *ar = new int[10];
   delete [4] ar;   // C2203
   // try the following line instead
   // delete [] ar;
}
```