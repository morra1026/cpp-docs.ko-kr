---
title: 컴파일러 오류 C2833 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2833
dev_langs:
- C++
helpviewer_keywords:
- C2833
ms.assetid: b9418ce1-e2ee-4599-8959-6fde89c27569
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 53360c1eaf81ad407589fbdb125d9e6fe017708e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070173"
---
# <a name="compiler-error-c2833"></a>컴파일러 오류 C2833

'operator o'를 인식할 수 있는 연산자 또는 형식이 아닙니다.

단어 `operator` 재정의 하려는 연산자나 변환 하려는 형식을 따라야 합니다.

관리 되는 형식에서 정의할 수 있는 연산자 목록을 참조 하세요 [사용자 정의 연산자](../../dotnet/user-defined-operators-cpp-cli.md)합니다.

다음 샘플에서는 C2833 오류가 생성 됩니다.

```
// C2833.cpp
// compile with: /c
class A {};

void operator ::* ();   // C2833
void operator :: ();   // OK
```