---
title: 컴파일러 오류 C3740 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3740
dev_langs:
- C++
helpviewer_keywords:
- C3740
ms.assetid: edb17a90-2307-4df6-943d-580460d26d2b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b6bda1392ae4ebe95c6038b8dd0ec322b32ba4d8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46044199"
---
# <a name="compiler-error-c3740"></a>컴파일러 오류 C3740

템플릿 원본 또는 이벤트를 수신할 수 없습니다.

템플릿 기반 클래스 또는 구조체를 포함할 수 없습니다 [이벤트](../../cpp/event-handling.md)합니다.

다음 샘플에서는 C3740 오류가 생성 됩니다.

```
// C3740.cpp
template <typename T>   // Delete the template specification
struct E {
   __event void f();   // C3740
};

int main() {
}
```