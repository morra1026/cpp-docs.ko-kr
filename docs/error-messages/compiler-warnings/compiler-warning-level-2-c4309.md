---
title: 컴파일러 경고 (수준 2) C4309 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4309
dev_langs:
- C++
helpviewer_keywords:
- C4309
ms.assetid: cb3f41ef-fd8a-4def-baa1-924e751fca68
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8b7eba833b547a54adc0644303ab51d3852740a8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041976"
---
# <a name="compiler-warning-level-2-c4309"></a>컴파일러 경고(수준 2) C4309

'conversion': 상수 값 잘림

형식 변환으로 할당 된 공간을 초과 하는 상수입니다. 상수에 대 한 더 큰 형식을 사용 해야 합니다.

다음 샘플에서는 C4309 오류가 생성 됩니다.

```
// C4309.cpp
// compile with: /W2
int main()
{
   char c = 128;   // C4309
}
```