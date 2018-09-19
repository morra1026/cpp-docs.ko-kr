---
title: 컴파일러 오류 C3469 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3469
dev_langs:
- C++
helpviewer_keywords:
- C3469
ms.assetid: e23b0e5c-c704-4e67-a868-bf02c2055d85
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f39889052b85ee6ab5595f388f939403fe3d2a46
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016990"
---
# <a name="compiler-error-c3469"></a>컴파일러 오류 C3469

'type': 제네릭 클래스는 전달할 수 없습니다.

제네릭 클래스에서 형식 전달을 사용할 수 없습니다.

자세한 내용은 [형식 전달 (C + + /cli CLI)](../../windows/type-forwarding-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 구성 요소를 만듭니다.

```
// C3469.cpp
// compile with: /clr /LD
generic<typename T>
public ref class GR {};

public ref class GR2 {};
```

## <a name="example"></a>예제

다음 샘플에서는 C3466를 생성합니다.

```
// C3469_b.cpp
// compile with: /clr /c
#using "C3469.dll"
[assembly:TypeForwardedTo(GR::typeid)];   // C3469
[assembly:TypeForwardedTo(GR2::typeid)];   // OK
```