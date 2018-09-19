---
title: 컴파일러 오류 C2504 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2504
dev_langs:
- C++
helpviewer_keywords:
- C2504
ms.assetid: c9e002a6-a4ee-4ba7-970e-edf4adb83692
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6fb11774f65454799761913babb428dc6a471743
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46054131"
---
# <a name="compiler-error-c2504"></a>컴파일러 오류 C2504

'class': 기본 클래스 정의 되지 않음

기본 클래스 선언 되었지만 정의 되지 않습니다.  가능한 원인:

1. 포함 파일이 없습니다.

1. 선언 되지 외부 기본 클래스 [extern](../../cpp/using-extern-to-specify-linkage.md)합니다.

다음 샘플에서는 C2504 오류가 생성 됩니다.

```
// C2504.cpp
// compile with: /c
class A;
class B : public A {};   // C2504
```

그래

```
class C{};
class D : public C {};
```