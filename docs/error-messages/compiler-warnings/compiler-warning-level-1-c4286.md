---
title: 컴파일러 경고 (수준 1) C4286 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4286
dev_langs:
- C++
helpviewer_keywords:
- C4286
ms.assetid: 93eadd6c-6f36-413b-ba91-c9aa2314685a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c1a796ee1956de0795f677afec90dd2a65bb3d1d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099527"
---
# <a name="compiler-warning-level-1-c4286"></a>컴파일러 경고(수준 1) C4286

'type1': 기본 클래스 ('type2')에 줄 번호에 의해 포착 됩니다

지정 된 예외 형식이 이전 처리기에 의해 처리 됩니다. 두 번째 catch에 대 한 형식이 첫 번째 형식에서 파생 됩니다. 파생된 클래스에 대 한 예외를 catch 하는 기본 클래스에 대 한 예외입니다.

## <a name="example"></a>예제

```
//C4286.cpp
// compile with: /W1
#include <eh.h>
class C {};
class D : public  C {};
int main()
{
    try
    {
        throw "ooops!";
    }
    catch( C ) {}
    catch( D ) {}  // warning C4286, D is derived from C
}
```