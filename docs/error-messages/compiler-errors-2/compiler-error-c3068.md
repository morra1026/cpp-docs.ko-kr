---
title: 컴파일러 오류 C3068 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3068
dev_langs:
- C++
helpviewer_keywords:
- C3068
ms.assetid: 613e3447-b4a8-4268-a661-297bed63ccdf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fdea26e204032c27f00639ee46a928c7bf084a4e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035625"
---
# <a name="compiler-error-c3068"></a>컴파일러 오류 C3068

'function': 'naked' 함수를 c + + 예외를 발생 한 경우에 필요한 해제는 개체를 포함할 수 없습니다

컴파일러에서 스택 해제를 수행할 수 없습니다.는 [naked](../../cpp/naked-cpp.md) 함수 및 c + + 예외 처리에 임시 개체 생성 되었기 때문에 예외가 발생 하는 함수 ([/EHsc](../../build/reference/eh-exception-handling-model.md)) 지정 되었습니다.

이 오류를 해결 하려면 다음 중 적어도 하나를 수행 합니다.

- /EHsc를 사용 하 여 컴파일되지 않습니다.

- 이 함수를 표시 하지 마십시오. `naked`합니다.

- 함수에서 임시 개체를 만들지 마십시오.

함수를 만드는 경우 임시 개체를 스택에 함수가 예외를 throw 하 고 c + + 예외 처리를 사용 하는 경우 예외가 throw 되 면 컴파일러 스택 위로 정리 됩니다.

예외가 throw 됩니다, 컴파일러에서 생성 한 코드를 프롤로그 호출을 에필로그와 naked 함수에 존재 하지 않는 함수에 대 한 실행 됩니다.

## <a name="example"></a>예제

다음 샘플에서는 C3068 오류가 생성 됩니다.

```
// C3068.cpp
// compile with: /EHsc
// processor: x86
class A {
public:
   A(){}
   ~A(){}
};

void b(A){}

__declspec(naked) void c() {
   b(A());   // C3068
};
```