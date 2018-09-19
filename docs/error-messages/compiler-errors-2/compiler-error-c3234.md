---
title: 컴파일러 오류 C3234 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3234
dev_langs:
- C++
helpviewer_keywords:
- C3234
ms.assetid: ebefc15a-e40d-424b-a3dd-d7e185d0ed7b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f701eb20743925913bf0eab754f2788e8bd3a9b6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46017051"
---
# <a name="compiler-error-c3234"></a>컴파일러 오류 C3234

제네릭 클래스는 제네릭 형식 매개 변수에서 상속할 수 없습니다.

제네릭 클래스는 제네릭 형식 매개 변수에서 상속할 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3234를 생성합니다.

```
// C3234.cpp
// compile with: /clr /c
generic <class T>
public ref class C : T {};   // C3234
// try the following line instead
// public ref class C {};
```