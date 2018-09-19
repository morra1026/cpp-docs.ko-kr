---
title: 컴파일러 오류 C3769 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3769
dev_langs:
- C++
helpviewer_keywords:
- C3769
ms.assetid: 341675e1-7428-4da6-8275-1b2f0a70dacc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: da57a883bcf66535a531e98e23b5927d37cadccd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46042231"
---
# <a name="compiler-error-c3769"></a>컴파일러 오류 C3769

'type': 중첩된 된 클래스의 이름은 바로 바깥쪽의 클래스를 사용할 수 없습니다

중첩된 클래스 바로 바깥쪽 클래스와 동일한 이름을 사용할 수 없습니다.

## <a name="example"></a>예제

다음 샘플 C3769를 생성합니다.

```
// C3769.cpp
// compile with: /c
class x {
   class x {};   // C3769
   class y {
      class x{};   // OK
   };
};
```