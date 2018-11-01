---
title: 컴파일러 경고(수준 1) C4489
ms.date: 11/04/2016
f1_keywords:
- C4489
helpviewer_keywords:
- C4489
ms.assetid: 43b51c8c-27b5-44c9-b974-fe4b48f4896f
ms.openlocfilehash: 4da96fd13fe9ba03c19808d32d3cdd9c73ec2b18
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50584732"
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