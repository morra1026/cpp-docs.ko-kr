---
title: 컴파일러 오류 C2129 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2129
dev_langs:
- C++
helpviewer_keywords:
- C2129
ms.assetid: 21a8223e-1d22-4baa-9ca1-922b7f751dd0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e86515a7d7c8954271578291c4ebcb1a52fc9863
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46054287"
---
# <a name="compiler-error-c2129"></a>컴파일러 오류 C2129

'function' 정적 함수 선언 되었지만 정의 되지 않았습니다.

전방 참조 하려고는 `static` 정의 되지 않은 함수입니다.

`static` 파일 범위 내에서 함수를 정의 해야 합니다. 를 다른 파일에서 함수를 정의 하는 경우 선언 되어야 합니다 `extern`합니다.