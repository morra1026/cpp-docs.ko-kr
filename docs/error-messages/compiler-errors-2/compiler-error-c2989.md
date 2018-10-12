---
title: 컴파일러 오류 C2989 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2989
dev_langs:
- C++
helpviewer_keywords:
- C2989
ms.assetid: 936303d8-eb3b-4746-82ec-2f18020a6f64
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 79da071b592a31ea3fe7ca486a7e02abc770f08e
ms.sourcegitcommit: d3c41b16bf05af2149090e996d8e71cd6cd55c7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/09/2018
ms.locfileid: "48890092"
---
# <a name="compiler-error-c2989"></a>컴파일러 오류 C2989

'class': 클래스 형식이 이미 비 클래스 형식으로 선언 되었습니다

제네릭 클래스 또는 템플릿 템플릿이나 제네릭이 아닌 클래스를 재정의합니다. 충돌에 대 한 헤더 파일을 확인 합니다.

다음 샘플에서는 C2989를 생성합니다.

```cpp
// C2989.cpp
// compile with: /c
class C{};

template <class T>
class C{};  // C2989
class C2{};
```

C2989는 제네릭을 사용할 때도 발생할 수 있습니다.

```cpp
// C2989b.cpp
// compile with: /clr /c
ref class GC1;

generic <typename T> ref class GC1;   // C2989
template <typename T> ref class GC2;

generic <typename T> ref class GC2;   // C2989
generic <typename T> ref class GCb;
template <typename T> ref class GC2;
generic <typename T> ref class GCc;
```