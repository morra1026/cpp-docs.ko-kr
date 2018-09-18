---
title: 컴파일러 오류 C3481 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3481
dev_langs:
- C++
helpviewer_keywords:
- C3481
ms.assetid: 5d09375a-5ed3-4b61-86ed-45e91fd734c7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 25634bb455a032ceff51d5e35f7a16e00e020326
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46066897"
---
# <a name="compiler-error-c3481"></a>컴파일러 오류 C3481

'var': 람다 캡처 변수가 없습니다.

컴파일러가 람다 식의 캡처 목록에 전달된 변수 정의를 찾을 수 없습니다.

### <a name="to-correct-this-error"></a>이 오류를 해결하려면

- 람다 식의 캡처 목록에서 변수를 제거합니다.

## <a name="example"></a>예제

다음 예제에서는 `n` 변수가 정의되지 않았기 때문에 C3481을 생성합니다.

```
// C3481.cpp

int main()
{
   [n] {}(); // C3481
}
```

## <a name="see-also"></a>참고 항목

[람다 식](../../cpp/lambda-expressions-in-cpp.md)