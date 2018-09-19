---
title: 컴파일러 경고 (수준 4) C4212 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4212
dev_langs:
- C++
helpviewer_keywords:
- C4212
ms.assetid: df781ea1-182d-4f9f-9a31-55b6ce80c711
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 107581742f1a60cfc015a9a1b8ccea8b2f89c7a3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074762"
---
# <a name="compiler-warning-level-4-c4212"></a>컴파일러 경고(수준 4) C4212

비표준 확장이 사용 됨: 줄임표 (...)를 사용 하는 함수 선언

함수 프로토타입은 인수의 변수 번호입니다. 함수 정의 되지 않습니다.

다음 샘플에서는 C4212 오류가 생성 됩니다.

```
// C4212.c
// compile with: /W4 /Ze /c
void f(int , ...);
void f(int i, int j) {}
```