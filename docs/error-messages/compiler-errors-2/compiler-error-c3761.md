---
title: 컴파일러 오류 C3761 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3761
dev_langs:
- C++
helpviewer_keywords:
- C3761
ms.assetid: 0c16f093-7a78-4838-b90b-0c67ef6e9270
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d543634bf91411fcaa6acaa0b53c8b4820c6c021
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46018407"
---
# <a name="compiler-error-c3761"></a>컴파일러 오류 C3761

'function': 'retval' 함수의 마지막 인수에만 나타날 수 있습니다

합니다 [retval](../../windows/retval.md) 목록의 마지막 인수 없는 함수 인수에 특성을 사용 했습니다.

다음 샘플에서는 C3761 오류가 생성 됩니다.

```
// C3761.cpp
#define _ATL_ATTRIBUTES 1
#include <atlbase.h>
#include <atlcom.h>

[ module(name=test) ];

[dispinterface]
__interface I
{
   [id(1)] HRESULT func([out, retval] int* i, [in] int j);
   // try the following line instead
   // [id(1)] HRESULT func([in] int i, [out, retval] int* j);
};

[coclass]
struct C : I {   // C3761
   HRESULT func(int* i, int j)
   // try the following line instead
   // HRESULT func(int j, int* i)
   {
      return S_OK;
   }
};

int main()
{
}
```