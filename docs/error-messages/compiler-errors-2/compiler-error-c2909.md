---
title: 컴파일러 오류 C2909 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2909
dev_langs:
- C++
helpviewer_keywords:
- C2909
ms.assetid: 1c9df8ae-925d-4002-a5f8-a71413c45f9e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f611a026d0a969f49eaf2dcd93ba081bae052d10
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46030887"
---
# <a name="compiler-error-c2909"></a>컴파일러 오류 C2909

'identifier': 함수 템플릿을 명시적으로 인스턴스화하려면 반환 형식이 있어야 합니다.

함수 템플릿의 명시적으로 인스턴스화하려면 해당 반환 형식의 명시적 사양이 있어야 합니다. 암시적 반환 형식 사양은 작동하지 않습니다.

다음 샘플에서는 C2909를 생성합니다.

```
// C2909.cpp
// compile with: /c
template<class T> int f(T);
template f<int>(int);         // C2909
template int f<int>(int);   // OK
```