---
title: 심각한 오류 C1026 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1026
dev_langs:
- C++
helpviewer_keywords:
- C1026
ms.assetid: 89bb9d40-673a-44aa-a9f4-b42c07b49d44
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: db9167383df48dad274ef8941defaa53f51d3bfa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068990"
---
# <a name="fatal-error-c1026"></a>심각한 오류 C1026

파서 스택 오버플로입니다. 프로그램이 너무 복잡합니다.

프로그램을 구문 분석 하는 데 필요한 공간을 컴파일러 스택 오버플로가 발생 했습니다.

식의 복잡성을 줄입니다.

- 중첩을 감소 시킵니다 `for` 고 `switch` 문입니다. 별도 함수에서 더 깊이 중첩 된 문을 배치 합니다.

- 쉼표 연산자 또는 함수 호출을 포함 하는 긴 식을 구분 합니다.