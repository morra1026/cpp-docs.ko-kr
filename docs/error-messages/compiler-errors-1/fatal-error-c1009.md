---
title: 심각한 오류 C1009 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1009
dev_langs:
- C++
helpviewer_keywords:
- C1009
ms.assetid: dcc8383c-3362-4c47-9c26-25d2451ebd53
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b1fbd8994be6fd86a764db400d8761a5d697079b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46037335"
---
# <a name="fatal-error-c1009"></a>심각한 오류 C1009

컴파일러 한계: 매크로가 너무 많이 중첩

컴파일러는 동시에 너무 많은 매크로 확장 하 려 했습니다. 컴파일러의 제한은 256 수준의 중첩 된 매크로입니다. 중첩 된 매크로 보다 간단한 매크로로 분할 합니다.