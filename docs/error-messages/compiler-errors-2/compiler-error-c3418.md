---
title: 컴파일러 오류 C3418 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3418
dev_langs:
- C++
helpviewer_keywords:
- C3418
ms.assetid: 54042c04-3c45-41c1-bad7-90f9ee05a21b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 26fa67da6f24e578319660c17cb48d7d715be408
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46033279"
---
# <a name="compiler-error-c3418"></a>컴파일러 오류 C3418

액세스 지정자 'specifier'는 지원되지 않습니다.

CLR 액세스 지정자를 잘못 지정했습니다.  자세한 내용은 참조 형식 표시 유형 및 멤버 표시 여부 [방법: 정의 사용할 클래스 및 구조체 (C + + CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3418을 생성합니다.

```cpp
// C3418.cpp
// compile with: /clr /c
ref struct m {
internal public:   // C3418
   void test(){}
};

ref struct n {
internal:   // OK
   void test(){}
};
```