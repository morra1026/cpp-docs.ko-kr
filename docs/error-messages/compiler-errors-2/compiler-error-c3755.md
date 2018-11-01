---
title: 컴파일러 오류 C3755
ms.date: 11/04/2016
f1_keywords:
- C3755
helpviewer_keywords:
- C3755
ms.assetid: 9317b55e-a52e-4b87-b915-5a208d6eda38
ms.openlocfilehash: 90dc3b7a0e1dbc4e0dc6c42ca722ca1db462fca9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50558212"
---
# <a name="compiler-error-c3755"></a>컴파일러 오류 C3755

'delegate': 대리자를 정의할 수 있습니다

A [delegate (c + + 구성 요소 확장)](../../windows/delegate-cpp-component-extensions.md) 선언할 수는 있지만 정의 되지 않았습니다.

## <a name="example"></a>예제

다음 샘플 C3755를 생성합니다.

```
// C3755.cpp
// compile with: /clr /c
delegate void MyDel() {};   // C3755
```

## <a name="example"></a>예제

C3755는 대리자 템플릿을 작성 하려는 경우에 발생할 수 있습니다. 다음 샘플 C3755를 생성합니다.

```
// C3755_b.cpp
// compile with: /clr /c
ref struct R {
   template<class T>
   delegate void D(int) {}   // C3755
};
```