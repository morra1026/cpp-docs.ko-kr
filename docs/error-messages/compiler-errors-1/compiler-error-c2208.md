---
title: 컴파일러 오류 C2208 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2208
dev_langs:
- C++
helpviewer_keywords:
- C2208
ms.assetid: 9ae704bc-bf70-45f1-8e47-0470f21edd4e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6721166efad2fc214ccf2c2a45ec2342b67c39e4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46101722"
---
# <a name="compiler-error-c2208"></a>컴파일러 오류 C2208

'type':이 형식을 사용 하 여 정의 된 멤버

형식 이름으로 확인 되는 식별자는 집계 선언 있지만 컴파일러는 멤버를 선언할 수 없습니다.

다음 샘플에서는 C2208 오류가 생성 됩니다.

```
// C2208.cpp
class C {
   C;   // C2208
   C(){}   // OK
};
```