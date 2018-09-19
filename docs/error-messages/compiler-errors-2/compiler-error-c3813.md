---
title: 컴파일러 오류 C3813 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3813
dev_langs:
- C++
helpviewer_keywords:
- C3813
ms.assetid: ffdbc489-71bf-4cd6-988c-f824c9ab3ceb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b8984feb5b657c26d2137eb9a3c648f1bcf442bf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46066273"
---
# <a name="compiler-error-c3813"></a>컴파일러 오류 C3813

property 선언은 WinRT 또는 관리되는 형식의 정의 내에서만 사용할 수 있습니다.

A [속성](../../dotnet/how-to-use-properties-in-cpp-cli.md) 관리 되는 또는 Windows 런타임 내 에서만 선언할 수 형식입니다. 네이티브 형식은 `property` 키워드를 지원하지 않습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3813 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```cpp
// C3813.cpp
// compile by using: cl /c /clr C3813.cpp
class A
{
   property int Int; // C3813
};

ref class B
{
   property int Int; // OK - declared within managed type
};
```