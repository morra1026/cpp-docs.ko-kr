---
title: 컴파일러 오류 C3453 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3453
dev_langs:
- C++
helpviewer_keywords:
- C3453
ms.assetid: dbefdbcf-f697-4239-b7a5-1d99b85e9e7f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7c35c039727cba004db879aea02c086cea4ddcec
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068807"
---
# <a name="compiler-error-c3453"></a>컴파일러 오류 C3453

'attribute': 'assembly' 한정자가 일치하지 않아 특성이 적용되지 않았습니다.

어셈블리 또는 모듈 수준 특성만 독립 실행형 명령으로 지정할 수 있습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3453을 생성합니다.

```
// C3453.cpp
// compile with: /clr /c
[assembly:System::CLSCompliant(true)]   // C3453
// try the following line instead
// [assembly:System::CLSCompliant(true)];
ref class X {};
```