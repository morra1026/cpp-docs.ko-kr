---
title: 컴파일러 오류 C2506 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2506
dev_langs:
- C++
helpviewer_keywords:
- C2506
ms.assetid: cfed21cd-2404-46f2-985e-d0c2c3820830
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4967c410dfdce781a4191c9ac848883228ba4d3a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46093417"
---
# <a name="compiler-error-c2506"></a>컴파일러 오류 C2506

'member': '__declspec(modifier)'이 기호에 적용할 수 없습니다

관리 되는 클래스의 정적 멤버에 대 한 프로세스당 또는 appdomain 별를 선언할 수 없습니다.

자세한 내용은 [appdomain](../../cpp/appdomain.md) 를 참조하세요.

## <a name="example"></a>예제

다음 샘플 C2506를 생성합니다.

```
// C2506.cpp
// compile with: /clr /c
ref struct R {
   __declspec(process) static int n;   // C2506
   int o;   // OK
};
```