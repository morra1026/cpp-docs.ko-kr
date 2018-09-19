---
title: 컴파일러 경고 (수준 4) C4092 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4092
dev_langs:
- C++
helpviewer_keywords:
- C4092
ms.assetid: 396ae826-a892-4327-bd66-f4762376d72b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 84aa73120dabd261d54e764d1e0bfe8bc9c561a0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46039616"
---
# <a name="compiler-warning-level-4-c4092"></a>컴파일러 경고 (수준 4) C4092

sizeof 'unsigned 반환합니다.

피연산자는 `sizeof` 연산자가 매우 큰 이므로 `sizeof` 부호 없는 반환 **긴**합니다. 이 경고는 Microsoft 확장에 발생 합니다 ([/Ze](../../build/reference/za-ze-disable-language-extensions.md)). ANSI 호환성 (/Za)에서 결과 대신 잘립니다.