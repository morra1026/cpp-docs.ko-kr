---
title: 컴파일러 경고 (수준 1) C4729 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4729
dev_langs:
- C++
helpviewer_keywords:
- C4729
ms.assetid: 36a0151f-f258-48d9-9444-ae6d41ff70a4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7d1f5b4fe452937ce74e56886a5214ff92f44af7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46096082"
---
# <a name="compiler-warning-level-1-c4729"></a>컴파일러 경고(수준 1) C4729

선형 그래프 기반 경고에 사용하기에는 함수가 너무 큽니다.

이 경고는 함수가 너무 커서 경고를 생성하는 상황을 안정적으로 검사하여 컴파일할 수 없는 경우에 생성됩니다. 이 경고는 [/Od](../../build/reference/od-disable-debug.md) 컴파일러 옵션을 사용한 경우에만 생성됩니다.

이 경고를 해결하려면 함수를 좀더 작은 함수로 나눕니다.