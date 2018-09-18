---
title: 컴파일러 오류 C3645 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3645
dev_langs:
- C++
helpviewer_keywords:
- C3645
ms.assetid: 346da528-ae86-4cd0-9654-f41bee26ac0d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2d310ab3a9a4bd0b31b9e6295a93a571a54f585b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068912"
---
# <a name="compiler-error-c3645"></a>컴파일러 오류 C3645

'function': __clrcall을 네이티브 코드로 컴파일된 함수에 사용할 수 없습니다

함수에서 일부 키워드의 현재 상태를 사용 하면 함수가를 네이티브로 컴파일하도록 합니다.

## <a name="example"></a>예제

다음 샘플 C3645를 생성합니다.

```
// C3645.cpp
// compile with: /clr /c
#pragma unmanaged
int __clrcall dog() {}   // C3645
```