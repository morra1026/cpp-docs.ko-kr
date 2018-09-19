---
title: 컴파일러 경고 (수준 4) C4201 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4201
dev_langs:
- C++
helpviewer_keywords:
- C4201
ms.assetid: 6156f508-9393-4d77-9e73-1ec3e1c32d0d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 702ce23333e29548e9bfe092c15ae60c5652168e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46096940"
---
# <a name="compiler-warning-level-4-c4201"></a>컴파일러 경고(수준 4) C4201

비표준 확장이 사용 됨: 이름이 없는 구조체/공용 구조체

Microsoft 확장 (/Ze)에서는 다른 구조체 또는 공용 구조체의 멤버로 선언 자 없이 구조체를 지정할 수 있습니다. 이러한 구조는 ANSI 호환성 오류를 생성 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).

## <a name="example"></a>예제

```
// C4201.cpp
// compile with: /W4
struct S
{
   float y;
   struct
   {
      int a, b, c;  // C4201
   };
} *p_s;

int main()
{
}
```