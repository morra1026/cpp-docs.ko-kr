---
title: 컴파일러 오류 C2821 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2821
dev_langs:
- C++
helpviewer_keywords:
- C2821
ms.assetid: e8d71988-a968-4484-94db-e8c3bad74a4a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 52525062a07c7c55dd323109be87667d9e0847d6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46098227"
---
# <a name="compiler-error-c2821"></a>컴파일러 오류 C2821

'operator new' 첫 번째 정식 매개 변수 'unsigned int' 이어야 합니다.

첫 번째 정식 매개 변수를 [new 연산자](../../standard-library/new-operators.md#op_new) 부호 없는 해야 `int`합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2821 오류가 생성 됩니다.

```cpp
// C2821.cpp
// compile with: /c
void * operator new( /* unsigned int,*/ void * );   // C2821
void * operator new( unsigned int, void * );
```