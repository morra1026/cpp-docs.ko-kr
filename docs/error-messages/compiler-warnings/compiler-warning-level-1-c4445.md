---
title: 컴파일러 경고(수준 1) C4445
ms.date: 11/04/2016
f1_keywords:
- C4445
helpviewer_keywords:
- C4445
ms.assetid: 535e92a0-ba08-4dfc-89b2-af2dcdd7caeb
ms.openlocfilehash: 6c1b4f4ae4f60d0c4281e0bbcfc9ca2b58d81851
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50611289"
---
# <a name="compiler-warning-level-1-c4445"></a>컴파일러 경고(수준 1) C4445

'function': WinRT 또는 관리되는 형식에서 가상 메서드는 private일 수 없습니다.

가상 함수가 private인 경우 파생된 형식에서 액세스할 수 없습니다. 이 오류를 해결하려면 가상 멤버 함수의 접근성을 보호됨이나 공용으로 변경합니다.