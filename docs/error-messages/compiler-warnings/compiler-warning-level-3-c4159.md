---
title: 컴파일러 경고 (수준 3) C4159 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4159
dev_langs:
- C++
helpviewer_keywords:
- C4159
ms.assetid: e2cf964e-f4b8-4b2c-9569-1abb94307232
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 43e3d63ad1d482222c4ffa7aa7435d0e660f3985
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43223320"
---
# <a name="compiler-warning-level-3-c4159"></a>컴파일러 경고 (수준 3) C4159

> #<a name="pragma-pragmapop--has-popped-previously-pushed-identifier-identifier"></a>pragma pragma(pop,...): 이전에 푸시한 식별자를 팝 했습니다 '*식별자*'

## <a name="remarks"></a>설명

소스 코드에 **푸시** 뒤에 pragma에 대 한 식별자를 사용 하 여 명령을 **pop** 식별자 없이 명령입니다. 따라서 *식별자* 표시 되 면, 및 이후 사용 됩니다 *식별자* 예기치 않은 동작이 발생할 수 있습니다.

## <a name="example"></a>예제

이 경고를 방지 하려면에 식별자를 제공 합니다 **pop** 명령입니다. 예를 들어:

```cpp
// C4159.cpp
// compile with: /W3
#pragma pack(push, f)
#pragma pack(pop)   // C4159

// using the identifier resolves the warning
// #pragma pack(pop, f)

int main()
{
}
```