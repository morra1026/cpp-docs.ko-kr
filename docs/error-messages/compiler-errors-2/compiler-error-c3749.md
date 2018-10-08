---
title: 컴파일러 오류 C3749 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3749
dev_langs:
- C++
helpviewer_keywords:
- C3749
ms.assetid: 3d26b468-4757-41b8-b5a2-78022a5295fb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7ac866d742734f5b6126315a0b79020c9ec7fb74
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48788398"
---
# <a name="compiler-error-c3749"></a>컴파일러 오류 C3749

'attribute': 함수 내에서 사용자 지정 특성을 사용할 수 없습니다

함수 내에서 사용자 지정 특성을 사용할 수 없습니다. 사용자 지정 특성에 대 한 자세한 내용은 항목을 참조 하세요 [특성](../../windows/attributes/attribute.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3749를 생성합니다.

```
// C3749a.cpp
// compile with: /clr /c
using namespace System;

[AttributeUsage(AttributeTargets::All)]
public ref struct ABC : public Attribute {
   ABC() {}
};

void f1() { [ABC]; };  // C3749
```
