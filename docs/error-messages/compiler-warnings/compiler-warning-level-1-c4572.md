---
title: 컴파일러 경고 (수준 1) C4572 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4572
dev_langs:
- C++
helpviewer_keywords:
- C4572
ms.assetid: 482dee5a-29bd-4fc3-b769-9dfd4cd2a964
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b87b3dd4264db9fd7ea3699f342358fa6d4d5aac
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076844"
---
# <a name="compiler-warning-level-1-c4572"></a>컴파일러 경고(수준 1) C4572

'...'를 사용 합니다 /clr [ParamArray] 특성은 사용 되지 않습니다. 대신

가변 인수 목록을 지정 하는 데 사용 되지 않는 스타일을 사용 했습니다. CLR을 컴파일할 때 대신 줄임표 구문을 사용 하 여 <xref:System.ParamArrayAttribute>입니다. 자세한 내용은 참조 하세요. [가변 인수 목록 (...) (C + + /CLI CLI) ](../../windows/variable-argument-lists-dot-dot-dot-cpp-cli.md).

## <a name="example"></a>예제

다음 샘플 C4572를 생성합니다.

```
// C4572.cpp
// compile with: /clr /W1
void Func([System::ParamArray] array<int> ^);   // C4572
void Func2(... array<int> ^){}   // OK

int main() {
   Func2(1, 2, 3);
}
```