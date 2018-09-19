---
title: 컴파일러 오류 C2733 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2733
dev_langs:
- C++
helpviewer_keywords:
- C2733
ms.assetid: 67f83561-c633-407c-a2ee-f9fd16e165bf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 42749c26f4a8a474f3dac076b80a1bfe71e89d58
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110447"
---
# <a name="compiler-error-c2733"></a>컴파일러 오류 C2733

'function' 없습니다 오버 로드 된 함수의 두 번째 C 링크

둘 이상의 오버 로드 된 함수는 C 링크를 사용 하 여 선언 됩니다. C 링크를 사용 하 여, 지정된 된 함수 하나만 형식의 외부 될 수 있습니다. 오버 로드 된 함수 데코 레이트 되지 않은 이름이 없으므로 C 프로그램에서 사용할 수 없습니다.

다음 샘플에서는 C2733 오류가 생성 됩니다.

```
// C2733.cpp
extern "C" {
   void F1(int);
}

extern "C" {
   void F1();   // C2733
   // try the following line instead
   // void F2();
}
```