---
title: 컴파일러 오류 C3824 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3824
dev_langs:
- C++
helpviewer_keywords:
- C3824
ms.assetid: b6c6adf1-0a29-401c-a06e-616fd50d4c37
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 03d42f80716b81f4409449262af650220b1ad92b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46083953"
---
# <a name="compiler-error-c3824"></a>컴파일러 오류 C3824

'member':이 형식 (함수 매개 변수, 반환 형식 또는 정적 멤버)이 컨텍스트에서 나타날 수 없습니다

고정 포인터는 함수 매개 변수, 반환 형식 수 없거나 또는 선언 `static`합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3824 오류가 생성 됩니다.

```
// C3824a.cpp
// compile with: /clr /c
void func() {
   static pin_ptr<int> a; // C3824
   pin_ptr<int> b; // OK
}
```
