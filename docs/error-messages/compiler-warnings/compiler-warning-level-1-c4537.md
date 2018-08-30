---
title: 컴파일러 경고 (수준 1) C4537 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4537
dev_langs:
- C++
helpviewer_keywords:
- C4537
ms.assetid: 9454493c-d419-475e-8f35-9c00233c9329
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 052d11d5bdf269d950abe1ef761adc055cbc6ce3
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43213365"
---
# <a name="compiler-warning-level-1-c4537"></a>컴파일러 경고(수준 1) C4537

> '*개체*': '*연산자*' 비 UDT 형식에 적용

## <a name="remarks"></a>설명

참조 개체 (사용자 정의 형식)가 필요 합니다. 여기서 전달 되었습니다. 참조 개체는 아닌 인라인 어셈블러 코드로 차이 만들 수 있습니다. 컴파일러 생성 코드 처럼 *개체* 인스턴스.

## <a name="example"></a>예제

다음 샘플 C4537 생성 및이 해결 하는 방법을 보여 줍니다.

```cpp
// C4537.cpp
// compile with: /W1 /c
// processor: x86
struct S {
    int member;
};

void f1(S &s) {
    __asm mov eax, s.member;   // C4537
    // try the following code instead
    // or, make the declaration "void f1(S s)"
    /*
    mov eax, s
    mov eax, [eax]s.member
    */
}
```