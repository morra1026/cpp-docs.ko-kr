---
title: 심각한 오류 C1509 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1509
dev_langs:
- C++
helpviewer_keywords:
- C1509
ms.assetid: 40dd100d-c6ba-451c-bd26-2c99ec1c36d6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 837ab5b7cf76b724726c6c52fbfe974d4da6ca85
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46033136"
---
# <a name="fatal-error-c1509"></a>심각한 오류 C1509

컴파일러 한계: 'function' 함수에 예외 처리기 상태가 너무 많습니다. 함수를 간소화 합니다.

코드는 예외 처리기 상태가 (32,768 상태)는 내부 한계를 초과합니다.

가장 일반적인 원인은 함수 클래스 사용자 정의 변수 및 산술 연산자의 복잡 한 식을 포함 합니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 일반적인 하위 식의 임시 변수를 할당 하 여 식을 간소화 합니다.

1. 함수를 좀 더 작은 함수로 분할 합니다.