---
title: 컴파일러 오류 C3550
ms.date: 11/04/2016
f1_keywords:
- C3550
helpviewer_keywords:
- C3550
ms.assetid: 9f2d5ffc-e429-41a1-89e3-7acc4fd47e14
ms.openlocfilehash: dbed14b9f2fa0f2163484edd8b5dfa330af9cbf1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50498883"
---
# <a name="compiler-error-c3550"></a>컴파일러 오류 C3550

이 컨텍스트에 일반 'decltype(auto)'만 사용할 수 있습니다.

`decltype(auto)`을 함수 반환 형식의 자리 표시자로 사용하는 경우 자체에서 사용되어야 합니다. 포인터 선언(`decltype(auto*)`), 참조 선언(`decltype(auto&)`) 또는 이러한 기타 모든 한정의 일부로 사용할 수 없습니다.

## <a name="see-also"></a>참고 항목

[auto](../../cpp/auto-cpp.md)