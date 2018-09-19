---
title: 컴파일러 오류 C2286 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2286
dev_langs:
- C++
helpviewer_keywords:
- C2286
ms.assetid: 078e0201-35cc-42e2-8dbc-6f8cf557b098
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2e4c3b8a71b29d0d1db5f3bc1eac642122844c22
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46089133"
---
# <a name="compiler-error-c2286"></a>컴파일러 오류 C2286

'identifier' 표현의 멤버에 대 한 포인터 선언이 무시 됩니다. '상속'-이미 설정 되어

클래스에 대 한 두 가지 다른 멤버에 대 한 포인터 표현이 존재 합니다.

자세한 내용은 [상속 키워드](../../cpp/inheritance-keywords.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2286을 생성합니다.

```
// C2286.cpp
// compile with: /c
class __single_inheritance X;
class __multiple_inheritance X;   // C2286
class  __multiple_inheritance Y;   // OK
```