---
title: 컴파일러 오류 C2129
ms.date: 11/04/2016
f1_keywords:
- C2129
helpviewer_keywords:
- C2129
ms.assetid: 21a8223e-1d22-4baa-9ca1-922b7f751dd0
ms.openlocfilehash: e55107419235420d272c738e9d8ef7cf277c11c9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50593458"
---
# <a name="compiler-error-c2129"></a>컴파일러 오류 C2129

'function' 정적 함수 선언 되었지만 정의 되지 않았습니다.

전방 참조 하려고는 `static` 정의 되지 않은 함수입니다.

`static` 파일 범위 내에서 함수를 정의 해야 합니다. 를 다른 파일에서 함수를 정의 하는 경우 선언 되어야 합니다 `extern`합니다.