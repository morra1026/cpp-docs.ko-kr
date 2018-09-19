---
title: 컴파일러 오류 C2535 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2535
dev_langs:
- C++
helpviewer_keywords:
- C2535
ms.assetid: a958f83e-e2bf-4a59-b44b-d406ec325d7e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 98e1920b2163a318fbdba3b64d56bf74a8cd809f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085903"
---
# <a name="compiler-error-c2535"></a>컴파일러 오류 C2535

'identifier': 이미 정의 되거나 선언 된 멤버 함수

이 오류는 여러 개 정의 또는 오버 로드 된 함수의 선언에 동일한 형식 매개 변수 목록을 사용 하 여 발생할 수 있습니다.

Dispose 함수로 인해 c2535 참조 [소멸자 및 종료자](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers) 자세한 내용은 합니다.

ATL 프로젝트를 컴파일하는 경우 기술 자료 문서 Q241852를 참조 하세요.

다음 샘플에서는 C2535를 생성합니다.

```
// C2535.cpp
// compile with: /c
class C {
public:
   void func();   // forward declaration
   void func() {}   // C2535
};
```