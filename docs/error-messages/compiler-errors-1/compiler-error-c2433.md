---
title: 컴파일러 오류 C2433 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2433
dev_langs:
- C++
helpviewer_keywords:
- C2433
ms.assetid: 7079fedd-6059-4125-82ef-ebe275f1f9d1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 081e63c83909319164a2903d8277a0b26a1e6901
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46059955"
---
# <a name="compiler-error-c2433"></a>컴파일러 오류 C2433

'identifier': 'modifier' 데이터 선언에서 허용 되지 않습니다

합니다 `friend`, `virtual`, 및 `inline` 데이터 선언에 대 한 한정자를 사용할 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2433 오류가 발생 합니다.

```
// C2433.cpp
class C{};

int main() {
   inline C c;   // C2433
}
```