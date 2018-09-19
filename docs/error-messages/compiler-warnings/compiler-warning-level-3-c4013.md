---
title: 컴파일러 경고 (수준 3) C4013 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4013
dev_langs:
- C++
helpviewer_keywords:
- C4013
ms.assetid: 9f9afc71-6e78-463d-9d66-3012d6a3cd5d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b491406111c7c5ba994bc0af6128b7f0578d52b7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46046500"
---
# <a name="compiler-warning-level-3-c4013"></a>컴파일러 경고 (수준 3) C4013

' function' 정의 되지 않았습니다. 가정 extern int를 반환 합니다.

컴파일러가 정의 되지 않은 함수에 대 한 호출을 발견 했습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 함수 이름의 철자가 잘못 되었습니다

1. 외부 함수를 프로토타입화 되지 않았습니다. `extern`