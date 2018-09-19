---
title: 컴파일러 오류 C3277 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3277
dev_langs:
- C++
helpviewer_keywords:
- C3277
ms.assetid: 8ac5f476-e30c-4879-92c6-f03cdbd74045
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5a346f6b2abce22a1238a1f9bc6f8ea9f961cb43
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46059066"
---
# <a name="compiler-error-c3277"></a>컴파일러 오류 C3277

관리 되지 않는 열거형 'enum' 관리 되는 'type' 내부에 정의할 수 없습니다.

관리 되는 형식 내에서 열거형 잘못 정의 되었습니다.

다음 샘플에서는 C3277 오류가 생성 됩니다.

```
// C3277a.cpp
// compile with: /clr
ref class A
{
   enum E {e1,e2};   // C3277
   // try the following line instead
   // enum class E {e1,e2};
};

int main()
{
}
```
