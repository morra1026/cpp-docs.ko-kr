---
title: 컴파일러 오류 C2588 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2588
dev_langs:
- C++
helpviewer_keywords:
- C2588
ms.assetid: 19a0cabd-ca13-44a5-9be3-ee676abf9bc4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d656dbde06d6052fd10611675f2cff8818cdb6e5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108575"
---
# <a name="compiler-error-c2588"></a>컴파일러 오류 C2588

':: ~ identifier': 잘못 된 전역 소멸자

소멸자는 클래스, 구조체 또는 공용 구조체 이외의 항목에 대 한 정의 됩니다. 이것은 허용되지 않습니다.

이 오류는 누락 된 클래스, 구조체 또는 공용 구조체 이름 범위 확인의 왼쪽에 의해 발생할 수 있습니다 (`::`) 연산자.

다음 샘플에서는 C2588 오류가 생성 됩니다.

```
// C2588.cpp
~F();   // C2588
```