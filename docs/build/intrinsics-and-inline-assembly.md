---
title: 내장 및 인라인 어셈블리
ms.date: 11/04/2016
ms.assetid: 8affd4bb-279d-46f3-851f-8be0a9c5ed3f
ms.openlocfilehash: 033225259c0a33414fe45eba313bb1f1c94eb379
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50515104"
---
# <a name="intrinsics-and-inline-assembly"></a>내장 및 인라인 어셈블리

하나는 x64에 대 한 제약 조건을 컴파일러는 인라인 어셈블러 지원 되지 않습니다. 이 즉, 함수는 컴파일러에서 지 원하는 내장 함수 또는 서브루틴으로 작성 해야 합니다 C 또는 c + +에서 쓸 수 없습니다. 특정 함수에는 성능에 민감한 나머지는 그렇지 않습니다. 성능이 중요 한 함수는 내장 함수로 구현 되어야 합니다.

컴파일러에서 지 원하는 내장 함수에 설명 되어 있습니다 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)합니다.

## <a name="see-also"></a>참고 항목

[x64 소프트웨어 규칙](../build/x64-software-conventions.md)