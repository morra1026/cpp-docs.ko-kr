---
title: 컴파일러 오류 C3530 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3530
dev_langs:
- C++
helpviewer_keywords:
- C3530
ms.assetid: 21be81ce-b699-4c74-81bc-80a0c34d2d5a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5866e2ea44b84f3afeb0cef8423abc28f8e056ab
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094795"
---
# <a name="compiler-error-c3530"></a>컴파일러 오류 C3530

'auto' 다른 형식 지정자를 사용 하 여 결합할 수 없습니다.

형식 지정자와 함께 사용 됩니다는 `auto` 키워드입니다.

### <a name="to-correct-this-error"></a>이 오류를 해결하려면

1. 사용 하는 변수 선언에 형식 지정자를 사용 하지 마십시오는 `auto` 키워드입니다.

## <a name="example"></a>예제

때문에 다음 예제에서는 생성 C3530 변수 `x` 둘 다를 사용 하 여 선언 되는 `auto` 키워드 및 형식 `int`, 이므로 예제로 컴파일됩니다 **/zc: auto**.

```
// C3530.cpp
// Compile with /Zc:auto
int main()
{
   auto int x;   // C3530
   return 0;
}
```

## <a name="see-also"></a>참고 항목

[auto 키워드](../../cpp/auto-keyword.md)