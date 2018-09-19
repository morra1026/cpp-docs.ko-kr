---
title: 컴파일러 경고 (수준 1) C4124 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4124
dev_langs:
- C++
helpviewer_keywords:
- C4124
ms.assetid: c08c3a65-9584-47a1-a147-44f00c4b230e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a69190487c22987ead2d00ec102785ed42ea93c4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46090934"
---
# <a name="compiler-warning-level-1-c4124"></a>컴파일러 경고 (수준 1) C4124

스택 검사 __fastcall 효율적입니다.

`__fastcall` 스택 검사를 사용할 수 있는 키워드를 사용 했습니다.

`__fastcall` 규칙 처리 속도가 빠른 코드도 생성 하지만 느린 코드 스택 검사를 수행 합니다. 사용 하는 경우 `__fastcall`를 사용 하 여 스택 검사 해제는 **check_stack** pragma 또는 /Gs 합니다.

이러한 조건에서 선언 된 첫 번째 함수에 대해서만 경고가 발생 합니다.