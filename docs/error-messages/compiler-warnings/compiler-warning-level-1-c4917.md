---
title: 컴파일러 경고 (수준 1) C4917 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4917
dev_langs:
- C++
helpviewer_keywords:
- C4917
ms.assetid: c05e2610-4a5d-4f4b-a99b-c15fd7f1d5f1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 741f847e4df8095e5e91e14dd67e36c6d161071d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46046266"
---
# <a name="compiler-warning-level-1-c4917"></a>컴파일러 경고(수준 1) C4917

'declarator': GUID 클래스, 인터페이스 또는 네임 스페이스를 사용 하 여 연결할 수만

다른 사용자 정의 구조 [클래스](../../cpp/class-cpp.md)를 [인터페이스](../../cpp/interface.md), 또는 [네임 스페이스](../../cpp/namespaces-cpp.md) GUID를 사용할 수 없습니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

## <a name="example"></a>예제

다음 코드 샘플에서는 C4917 오류가 생성 됩니다.

```cpp
// C4917.cpp
// compile with: /W1
#pragma warning(default : 4917)
__declspec(uuid("00000000-0000-0000-0000-000000000001")) struct S
{
} s;   // C4917, don't put uuid on a struct

int main()
{
}
```