---
title: 컴파일러 오류 C2449 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2449
dev_langs:
- C++
helpviewer_keywords:
- C2449
ms.assetid: 544bf0b6-daa0-40e8-9f21-8e583d472a2d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3e92638eaca1fe951d6b67da7563930214198926
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46018771"
---
# <a name="compiler-error-c2449"></a>컴파일러 오류 C2449

찾을 ' {0} ' 파일 범위 (함수 헤더가 없습니다.?)

중괄호는 파일 범위에서 발생합니다.

이 오류는 함수 헤더와 함수 정의의 여는 중괄호 사이 세미콜론을 하 여 발생할 수 있습니다.

다음 샘플에서는 C2499 오류가 생성 됩니다.

```
// C2449.c
// compile with: /c
void __stdcall func(void) {}   // OK
void __stdcall func(void);  // extra semicolon on this line
{                         // C2449 detected here
```