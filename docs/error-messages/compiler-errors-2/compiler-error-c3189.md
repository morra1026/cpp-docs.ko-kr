---
title: 컴파일러 오류 C3189 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3189
dev_langs:
- C++
helpviewer_keywords:
- C3189
ms.assetid: b254de79-931e-4a59-a9f4-1c690d90ca5e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c4666a16aed6d26f1cf38e4b32523c7c36948274
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46093872"
---
# <a name="compiler-error-c3189"></a>컴파일러 오류 C3189

' typeid\<추상 선언 자 입력 >':이 구문은 지원 되지 않는, 사용:: typeid 대신

사용 되지 않는 형태로 [typeid](../../windows/typeid-cpp-component-extensions.md) 된 새 형식을 사용 하 여 사용 합니다.

다음 샘플에서는 C3189 오류가 생성 됩니다.

```
// C3189.cpp
// compile with: /clr
int main() {
   System::Type^ t  = typeid<System::Object>;   // C3189
   System::Type^ t2  = System::Object::typeid;   // OK
}
```