---
title: 심각한 오류 C1026
ms.date: 11/04/2016
f1_keywords:
- C1026
helpviewer_keywords:
- C1026
ms.assetid: 89bb9d40-673a-44aa-a9f4-b42c07b49d44
ms.openlocfilehash: b1a659967a9a62cb79e1084f7d1fa1729bae14da
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50666190"
---
# <a name="fatal-error-c1026"></a>심각한 오류 C1026

파서 스택 오버플로입니다. 프로그램이 너무 복잡합니다.

프로그램을 구문 분석 하는 데 필요한 공간을 컴파일러 스택 오버플로가 발생 했습니다.

식의 복잡성을 줄입니다.

- 중첩을 감소 시킵니다 `for` 고 `switch` 문입니다. 별도 함수에서 더 깊이 중첩 된 문을 배치 합니다.

- 쉼표 연산자 또는 함수 호출을 포함 하는 긴 식을 구분 합니다.