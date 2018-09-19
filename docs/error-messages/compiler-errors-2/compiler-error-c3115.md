---
title: 컴파일러 오류 C3115 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3115
dev_langs:
- C++
helpviewer_keywords:
- C3115
ms.assetid: 51726145-9782-4ec9-84b9-286f366d9cbd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: da47a6987a1b540dc42b154c1a181c67e1524043
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46090687"
---
# <a name="compiler-error-c3115"></a>컴파일러 오류 C3115

'attribute':이 특성은 'construct'에서 허용 되지 않습니다

특성은 의도 하지 않은 구문에 적용 되었습니다.  참조 [용도별 특성](../../windows/attributes-by-usage.md) 자세한 내용은 합니다.

## <a name="example"></a>예제

다음 샘플 C3115를 생성합니다.

```
// C3115.cpp
// compile with: /c
#include <unknwn.h>
[module(name="xx")];

[object, helpstringdll(xx.dll), uuid("00000000-0000-0000-0000-000000000001")]   // C3115
// try the following line instead
// [object, uuid("00000000-0000-0000-0000-000000000001")]
__interface IMyI {
   HRESULT xx();
};
```