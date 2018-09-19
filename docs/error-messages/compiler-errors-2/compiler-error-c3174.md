---
title: 컴파일러 오류 C3174 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3174
dev_langs:
- C++
helpviewer_keywords:
- C3174
ms.assetid: fe6b3b5a-8196-485f-a45f-0b2e51df4086
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1ca73c1fa16f2cc8b25f355705c7f0a72916158d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46105190"
---
# <a name="compiler-error-c3174"></a>컴파일러 오류 C3174

모듈 특성을 지정 하지 않았습니다.

Visual c + + 특성을 사용 하는 프로그램을 사용 하지 않았습니다 합니다 [모듈](../../windows/module-cpp.md) 특성을 사용 하는 프로그램에 필요한 특성입니다.

다음 샘플에서는 C3174 오류가 생성 됩니다.

```
// C3174.cpp
// C3174 expected
// uncomment the following line to resolve this C3174
// [module(name="x")];
[export]
struct S
{
   int i;
};

int main()
{
}
```