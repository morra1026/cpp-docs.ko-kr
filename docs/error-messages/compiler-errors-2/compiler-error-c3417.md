---
title: 컴파일러 오류 C3417 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3417
dev_langs:
- C++
helpviewer_keywords:
- C3417
ms.assetid: 3e7869ea-8948-42fb-ba30-6ccafe499c35
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8b21636c3500625f262355750d32aa0fa3faeb5d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46073852"
---
# <a name="compiler-error-c3417"></a>컴파일러 오류 C3417

'member': 값 형식은 사용자 정의 특수 멤버 함수를 포함할 수 없습니다

값 형식의 기본 인스턴스 생성자, 소멸자 또는 복사 생성자와 같은 함수를 포함할 수 없습니다.

다음 샘플에서는 C3517 오류가 생성 됩니다.

```
// C3417.cpp
// compile with: /clr /c
value class VC {
   VC(){}   // C3417

   // OK
   static VC(){}
   VC(int i){}
};
```