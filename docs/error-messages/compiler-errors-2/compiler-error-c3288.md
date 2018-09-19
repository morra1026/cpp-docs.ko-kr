---
title: 컴파일러 오류 C3288 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3288
dev_langs:
- C++
helpviewer_keywords:
- C3288
ms.assetid: ed08a540-9751-46e1-9cbe-c51d6a49ffab
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 36412510efcedd765ad44b4aab61e6a7d64155fb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46079936"
---
# <a name="compiler-error-c3288"></a>컴파일러 오류 C3288

'type': 핸들 형식에 대 한 역참조가 잘못 되었습니다.

컴파일러는 핸들 형식의 잘못 된 역참조를 발견 했습니다. 핸들 형식 역참조 하 고 참조를 할당할 수 있습니다. 자세한 내용은 [추적 참조 연산자](../../windows/tracking-reference-operator-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3288를 생성합니다.

```
// C3288.cpp
// compile with: /clr
ref class R {};
int main() {
   *(System::Object^) nullptr;   // C3288

// OK
   (System::Object^) nullptr;   // OK
   R^ r;
   R% pr = *r;
}
```