---
title: 컴파일러 경고 (수준 3) C4638 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4638
dev_langs:
- C++
helpviewer_keywords:
- C4638
ms.assetid: 2c07923a-e103-4e40-bd11-fdfed428a5ec
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 29febc17f041fee27064fc085896c892eecd5c56
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43198234"
---
# <a name="compiler-warning-level-3-c4638"></a>컴파일러 경고(수준 3) C4638

> XML 문서 주석 대상: 알 수 없는 기호에 대 한 참조가 '*기호*'

## <a name="remarks"></a>설명

컴파일러에서 기호를 확인할 수 없습니다 (*기호*). 컴파일할 때 기호가 유효해야 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4638을 생성합니다.

```cpp
// C4638.cpp
// compile with: /clr /doc /LD /W3
using namespace System;

/// Text for class MyClass.
public ref class MyClass {
public:
   /// <summary> Text </summary>
   /// <see cref="aSymbolThatAppearsNowhereInMyProject"/>
   // Try the following line instead:
   // /// <see cref="System::Console::WriteLine"/>
   void MyMethod() {}
};   // C4638
```