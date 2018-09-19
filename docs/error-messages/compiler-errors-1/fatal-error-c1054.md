---
title: 심각한 오류 C1054 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1054
dev_langs:
- C++
helpviewer_keywords:
- C1054
ms.assetid: 9cfb7307-b22a-4418-b7c0-2621b0ab5b1b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 439019b1f510127ae54e77d445d59e86be09a49b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46101971"
---
# <a name="fatal-error-c1054"></a>심각한 오류 C1054

컴파일러 한계: 이니셜라이저가 너무 많이 중첩

이니셜라이저 (초기화 되는 형식의 조합에 따라 10 ~ 15 개 수준)에 중첩 한계를 초과 하는 코드입니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 중첩을 줄이기 위해 초기화 되는 데이터 형식을 간소화 합니다.

1. 선언 후 별도 문에서 변수를 초기화 합니다.