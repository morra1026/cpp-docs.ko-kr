---
title: 컴파일러 오류 C2500 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2500
dev_langs:
- C++
helpviewer_keywords:
- C2500
ms.assetid: 6bff8161-dc9a-48ca-91f1-fd2eefdbbc93
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9b7e24ca520796b63171fe63c2bf841fe8776845
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026675"
---
# <a name="compiler-error-c2500"></a>컴파일러 오류 C2500

'identifier1': 'identifier2' 이미 직접 기본 클래스입니다.

클래스 또는 구조체의 기본 클래스 목록에 두 번 이상 나타납니다.

직접 기본에는 기본 목록에 나오는 하나입니다. 간접 기본은 기본 목록에 클래스 중 하나의 기본 클래스입니다.

클래스는 직접 기본 클래스를 두 번 이상 지정할 수 없습니다. 클래스는 두 번 이상 간접 기본 클래스도 사용할 수 있습니다.

다음 샘플에서는 C2500 오류가 생성 됩니다.

```
// C2500.cpp
// compile with: /c
class A {};
class B : public A, public A {};    // C2500

// OK
class C : public A {};
class D : public A {};
class E : public C, public D {};
```