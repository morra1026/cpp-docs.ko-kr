---
title: 컴파일러 오류 C2601 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2601
dev_langs:
- C++
helpviewer_keywords:
- C2601
ms.assetid: 88275582-5f37-45d7-807d-05f06ba00965
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 522abe9c3cb4b9922a6b307055a3d85f40253793
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062958"
---
# <a name="compiler-error-c2601"></a>컴파일러 오류 C2601

'function': 지역 함수 정의가 올바르지 않습니다.

코드는 함수 내에서 함수를 정의 하려고 시도 합니다.

또는 C2601 오류의 위치 앞에 소스 코드에서 하는 추가 중괄호 있을 수 있습니다.

다음 샘플에서는 C2601 오류가 생성 됩니다.

```
// C2601.cpp
int main() {
   int i = 0;

   void funcname(int j) {   // C2601
      j++;
   }
}
```