---
title: 컴파일러 오류 C2878 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2878
dev_langs:
- C++
helpviewer_keywords:
- C2878
ms.assetid: 83ee3de1-f554-49e8-a840-1f550cee7f69
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4715d7eb83ffac3272f6187c6b67bae1af97ba64
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46021423"
---
# <a name="compiler-error-c2878"></a>컴파일러 오류 C2878

'name': 네임 스페이스 또는 클래스 이름이 없습니다.

네임 스페이스 또는 정의 되지 않은 클래스를 참조를 했습니다.

다음 샘플에서는 C2878 오류가 생성 됩니다.

```
// C2878.cpp
// compile with: /c
namespace A {}
namespace B = C;   // C2878 namespace C doesn't exist
namespace B = A;
```