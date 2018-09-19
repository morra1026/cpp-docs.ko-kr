---
title: 컴파일러 오류 C2995 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2995
dev_langs:
- C++
helpviewer_keywords:
- C2995
ms.assetid: a57cdfe0-b40b-4a67-a95c-1a49ace4842b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b63028629dd23d3bae20da0b1470cf3239c00306
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46109380"
---
# <a name="compiler-error-c2995"></a>컴파일러 오류 C2995

'function': 함수 템플릿이 이미 정의되었습니다.

템플릿 클래스의 각 멤버 함수에 대한 정의가 하나뿐인지 확인합니다.

다음 샘플에서는 C2995를 생성합니다.

```
// C2995.cpp
// compile with: /c
template <class T>
void Test(T x){}

template <class T> void Test(T x){}   // C2995
template <class T> void Test2(T x){}   // OK
```