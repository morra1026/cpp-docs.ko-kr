---
title: 컴파일러 오류 C2714 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2714
dev_langs:
- C++
helpviewer_keywords:
- C2714
ms.assetid: 401a5a42-660c-4bad-9d63-1a2d092bc489
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8a5a8a2157fc574b9a43688bfc8fa9adcbcb676f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108497"
---
# <a name="compiler-error-c2714"></a>컴파일러 오류 C2714

__alignof(void) 허용 되지 않습니다.

잘못 된 값은 운영자에 게 전달 되었습니다.

참조 [__alignof 연산자](../../cpp/alignof-operator.md) 자세한 내용은 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2714 오류가 발생 합니다.

```
// C2714.cpp
int main() {
   return __alignof(void);   // C2714
   return __alignof(char);   // OK
}
```