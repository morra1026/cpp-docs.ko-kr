---
title: 컴파일러 오류 C3457 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3457
dev_langs:
- C++
helpviewer_keywords:
- C3457
ms.assetid: 5c1e366a-fa75-4cca-b9a3-86d4ebe4090e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 794c3deb042c383f3802ce32f3f7c4580f6061a6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46021501"
---
# <a name="compiler-error-c3457"></a>컴파일러 오류 C3457

'attribute': 특성은 명명되지 않은 인수를 지원하지 않습니다.

CLR 사용자 지정 특성 또는 컴파일러 특성과 달리 소스 주석 특성은 명명된 인수만 지원합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3457을 생성합니다.

```
#include "SourceAnnotations.h"
[vc_attributes::Post( 1 )] int f();   // C3457
[vc_attributes::Post( Valid=vc_attributes::Yes )] int f2();   // OK
```