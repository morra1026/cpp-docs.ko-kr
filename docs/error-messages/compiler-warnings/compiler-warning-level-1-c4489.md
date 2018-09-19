---
title: 컴파일러 경고 (수준 1) C4489 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4489
dev_langs:
- C++
helpviewer_keywords:
- C4489
ms.assetid: 43b51c8c-27b5-44c9-b974-fe4b48f4896f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bc019c618a5e4b8a453652573f6f407279792d56
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46023256"
---
# <a name="compiler-warning-level-1-c4489"></a>컴파일러 경고(수준 1) C4489

'specifier': 인터페이스 메서드 'method';에서 허용 되지 않습니다 재정의 지정자는 ref 클래스와 값 클래스 메서드에만 사용할 수

지정자 키워드는 인터페이스 메서드에 잘못 사용 되었습니다.

자세한 내용은 [재정의 지정자](../../windows/override-specifiers-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C4489를 생성합니다.

```
// C4489.cpp
// compile with: /clr /c /W1
public interface class I {
   void f() new;   // C4489
   virtual void b() override;   // C4489

   void g();   // OK
};
```