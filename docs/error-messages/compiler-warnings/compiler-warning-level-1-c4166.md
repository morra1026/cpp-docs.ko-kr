---
title: 컴파일러 경고 (수준 1) C4166 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4166
dev_langs:
- C++
helpviewer_keywords:
- C4166
ms.assetid: 4e5398a1-d913-4791-a470-06fc99c36ac5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7c6112c684dc4896393b35309a0a3af7eedd455d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051999"
---
# <a name="compiler-warning-level-1-c4166"></a>컴파일러 경고(수준 1) C4166

**생성자/소멸자에 대한 호출 규칙이 잘못되었습니다.**

생성자 및 소멸자에는 플랫폼에 대한 기본값 이외의 다른 호출 규칙을 사용할 수 없습니다(명시적으로 **__clrcall**을 지정하는 경우 제외).