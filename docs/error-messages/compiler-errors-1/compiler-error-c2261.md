---
title: 컴파일러 오류 C2261 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2261
dev_langs:
- C++
helpviewer_keywords:
- C2261
ms.assetid: 60969482-9e83-49b5-9631-a04bc844da12
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2ed43dc43fb6ceaf514a8e7452b06eb7bdaf7362
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051648"
---
# <a name="compiler-error-c2261"></a>컴파일러 오류 C2261

'string': 어셈블리 참조가 잘못 되어 확인할 수 없습니다

값이 잘못 되었습니다.

<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> friend 어셈블리를 지정 하는 데 사용 됩니다. 예를 들어 a.dll를 b.dll를 friend 어셈블리로 지정 하려는 경우 지정 a.dll) (에: InternalsVisibleTo("b") 합니다. 런타임에서 b.dll a.dll (제외 개인 형식)에서 모든 항목에 액세스할 수 있게 합니다.

Friend 어셈블리를 지정 하는 경우에 올바른 구문에 자세한 내용은 참조 하십시오 [Friend 어셈블리 (c + +)](../../dotnet/friend-assemblies-cpp.md)합니다.

## <a name="example"></a>예제

다음 샘플 C2261를 생성합니다.

```
// C2261.cpp
// compile with: /clr /c
using namespace System::Runtime::CompilerServices;
[assembly: InternalsVisibleTo("a,a,a")];   // C2261
[assembly: InternalsVisibleTo("a.a")];   // OK
[assembly: InternalsVisibleTo("a")];   // OK
```