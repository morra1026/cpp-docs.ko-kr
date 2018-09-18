---
title: 컴파일러 오류 C2379 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2379
dev_langs:
- C++
helpviewer_keywords:
- C2379
ms.assetid: 37dc3015-a4af-4341-bbf3-da6150df7e51
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ec340a5a48705eb91bf5bf72ec20ad382f4b262c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032447"
---
# <a name="compiler-error-c2379"></a>컴파일러 오류 C2379

정식 매개 변수 번호의 형식이 다릅니다.

지정 된 매개 변수 형식의 이전 선언에서 형식 사용 하 여 기본 프로 모션을 통해 호환 되지 않습니다. 이것은 ANSI C에서 오류 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) 및 Microsoft 확장을 사용 하 여 경고 (**/Ze**).

다음 샘플에서는 C2379를 생성합니다.

```
// C2379.c
// compile with: /Za
void func();
void func(char);   // C2379, char promotes to int
```