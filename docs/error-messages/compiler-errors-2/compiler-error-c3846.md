---
title: 컴파일러 오류 C3846 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3846
dev_langs:
- C++
helpviewer_keywords:
- C3846
ms.assetid: c470f8a5-106b-4efb-b8dc-e1319e04130f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7f8b44661534dca1beb39c0407f882d41f1f503c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055132"
---
# <a name="compiler-error-c3846"></a>컴파일러 오류 C3846

'symbol': 'assembly2'에서 기호를 가져올 수 없습니다: 'symbol' 어셈블리가 'assembly1'에서 이미 가져온 대로

참조 된 어셈블리에서 이전에 가져온 참조 된 어셈블리에서 기호를 가져올 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3846 오류가 생성 됩니다.

```
// C3846a.cpp
// compile with: /LD /clr
public ref struct G
{
};
```

하 고이 컴파일합니다.

```
// C3846b.cpp
// compile with: /clr
#using "c3846a.dll"
#using "c3846a.obj"   // C3846

int main()
{
}
```
