---
title: 컴파일러 경고 (수준 1) C4661 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4661
dev_langs:
- C++
helpviewer_keywords:
- C4661
ms.assetid: 603bb8b7-356d-4eef-924b-64d769bac5bd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1823e23f3afc432982d0d68eee3fe080fe52d719
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045759"
---
# <a name="compiler-warning-level-1-c4661"></a>컴파일러 경고(수준 1) C4661

'identifier': 명시적 템플릿 인스턴스화 요청에 대 한 제공 된 적합 한 정의가 없습니다

템플릿 클래스의 멤버 정의 되지 않았습니다.

## <a name="example"></a>예제

```
// C4661.cpp
// compile with: /W1 /LD
template<class T> class MyClass {
public:
   void i();   // declaration but not definition
};
template MyClass< int >;  // C4661
```