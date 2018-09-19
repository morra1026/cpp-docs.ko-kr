---
title: 컴파일러 오류 C3765 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3765
dev_langs:
- C++
helpviewer_keywords:
- C3765
ms.assetid: feadee7a-fcfb-402c-af2f-0e656f814a13
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cac3930e4f5ec42587a9f557adc7a82d750b3819
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46042132"
---
# <a name="compiler-error-c3765"></a>컴파일러 오류 C3765

'event': event_receiver로 표시 된 'type' 클래스/구조체에서 이벤트를 정의할 수 없습니다

클래스에 표시 되는 경우는 [event_receiver](../../windows/event-receiver.md) 특성 클래스를 포함할 수 없습니다는 [__event](../../cpp/event.md) 선언 합니다.

다음 샘플에서는 C3765 오류가 생성 됩니다.

```
// C3765.cpp
[event_receiver(native)]
struct ER2 {
   __event void f();   // C3765
   __event void b(int);   // C3765
};
```