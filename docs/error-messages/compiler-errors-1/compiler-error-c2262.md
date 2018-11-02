---
title: 컴파일러 오류 C2262
ms.date: 11/04/2016
f1_keywords:
- C2262
helpviewer_keywords:
- C2262
ms.assetid: 727d1c6e-53e8-40e5-b7b8-6a7ac2011727
ms.openlocfilehash: 12272c21adac0e326cb8b149b359584197577941
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50567065"
---
# <a name="compiler-error-c2262"></a>컴파일러 오류 C2262

'attribute_specifiers': InternalsVisibleTo 선언에는 버전, 문화권 또는 프로세서 아키텍처를 지정할 수 없습니다.

<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> 특성을 올바르게 지정하지 않았습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2262를 생성합니다.

```
// C2262.cpp
// compile with: /clr /c
using namespace System::Runtime::CompilerServices;
[assembly: InternalsVisibleTo("assembly_name, version=1.2.3.7")];   // C2262
[assembly: InternalsVisibleTo("assembly_name ")];   // OK
```