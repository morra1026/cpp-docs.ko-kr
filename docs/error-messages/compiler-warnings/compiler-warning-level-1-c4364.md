---
title: 컴파일러 경고 (수준 1) C4364 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4364
dev_langs:
- C++
helpviewer_keywords:
- C4364
ms.assetid: 1477634c-d60f-4570-ad16-1aaeae24ac7f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e37c7f37e1b51296bd5c3ae2cbdb85a93326f027
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087255"
---
# <a name="compiler-warning-level-1-c4364"></a>컴파일러 경고(수준 1) C4364

\#as_friend 특성 없이 location(line_number)에서 이전에 표시 하는 ' file' 어셈블리에 대 한 사용 as_friend 적용 되지 않음

A `#using` 지시문을 지정 된 메타 데이터 파일에 대 한 반복 하지만 `as_friend` 한정자는 처음에 사용 되지 않았던; 컴파일러는 두 번째 무시 `as_friend`.

자세한 내용은 [Friend 어셈블리 (c + +)](../../dotnet/friend-assemblies-cpp.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 구성 요소를 만듭니다.

```
// C4364.cpp
// compile with: /clr /LD
ref class A {};
```

## <a name="example"></a>예제

다음 샘플에서는 C4364 오류가 발생 합니다.

```
// C4364_b.cpp
// compile with: /clr /W1 /c
#using " C4364.dll"
#using " C4364.dll" as_friend   // C4364
```