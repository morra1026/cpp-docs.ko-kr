---
title: 컴파일러 오류 C3141 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3141
dev_langs:
- C++
helpviewer_keywords:
- C3141
ms.assetid: b4fd65c3-50cc-46cd-8de0-6a6d24cb9cda
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fda465b7cad2b46510b6f5e2dc4dc5d5fe82ecaf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46038323"
---
# <a name="compiler-error-c3141"></a>컴파일러 오류 C3141

'interface_name': 인터페이스에는 공용 상속만 지원

사용 하 여 정의 된 인터페이스를 [인터페이스 (또는 __interface)](../../cpp/interface.md) 키워드에는 공용 상속만 지원 합니다.

다음 샘플에서는 C3141 오류가 생성 됩니다.

```
// C3141.cpp
__interface IBase {};
__interface IDerived1 : protected IBase {};  // C3141
__interface IDerived2 : private IBase {};    // C3141
```