---
title: 컴파일러 오류 C3648 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3648
dev_langs:
- C++
helpviewer_keywords:
- C3648
ms.assetid: 5d042989-41cb-4cd0-aa50-976b70146aaf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6cb86e4b34295a31e6c2d9a6fb8567efd9fbfe12
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110499"
---
# <a name="compiler-error-c3648"></a>컴파일러 오류 C3648

이 명시적 재정의 구문은 /clr: oldsyntax 필요

최신 관리 되는 구문에 대 한를 컴파일할 때 컴파일러에서 명시적 검색에 더 이상 지원 되지 않는 이전 버전에 대 한 구문을 재정의 합니다.

자세한 내용은 [명시적으로 재정의](../../windows/explicit-overrides-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3648 오류가 생성 됩니다.

```
// C3648.cpp
// compile with: /clr
public interface struct I {
   void f();
};

public ref struct R : I {
   virtual void I::f() {}   // C3648
   // try the following line instead
   // virtual void f() = I::f{}
};
```