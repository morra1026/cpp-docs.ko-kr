---
title: 컴파일러 경고 (수준 3) C4306 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4306
dev_langs:
- C++
helpviewer_keywords:
- C4306
ms.assetid: 5b2192d7-402d-4b6d-8619-08105e7dcac7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ab5372213819375a6c1fec3cfc43970415b6486a
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43219996"
---
# <a name="compiler-warning-level-3-c4306"></a>컴파일러 경고(수준 3) C4306

> '*식별자*': 변환할 '*type1*'to'*type2*' 큰 크기의

식별자가 형식 보다 큰 포인터에 캐스팅 합니다. 새 형식의 채워지지 않은 상위 비트가 0으로 채워진 됩니다.

이 경고는 의도 하지 않은 변환을 나타낼 수 있습니다. 결과 포인터는 유효 하지 않을 수 있습니다.