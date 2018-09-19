---
title: 컴파일러 오류 C3834 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3834
dev_langs:
- C++
helpviewer_keywords:
- C3834
ms.assetid: 059e0dc4-300b-4e74-b6c2-41a57831fe2a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1032c8210cc3df8f9000452ebe18576a10cf5437
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072760"
---
# <a name="compiler-error-c3834"></a>컴파일러 오류 C3834

잘못 된 명시적 고정 포인터로 캐스팅 고정된 된 지역 변수를 대신 사용

고정 포인터로 명시적 캐스트는 허용 되지 않습니다.

## <a name="example"></a>예제

다음 샘플 C3834를 생성합니다.

```
// C3834.cpp
// compile with: /clr
int main() {
   int x = 33;

   pin_ptr<int> p = safe_cast<pin_ptr<int> >(&x);   // C3834
   pin_ptr<int> p2 = &x;   // OK
}
```
