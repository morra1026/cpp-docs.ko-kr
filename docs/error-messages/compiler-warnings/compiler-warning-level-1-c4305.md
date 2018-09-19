---
title: 컴파일러 경고 (수준 1) C4305 | Microsoft Docs
ms.custom: ''
ms.date: 1/17/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4305
dev_langs:
- C++
helpviewer_keywords:
- C4305
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 88ae0fb38b7e6af14525906e90486a68ce22ee56
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086826"
---
# <a name="compiler-warning-level-1-c4305"></a>컴파일러 경고(수준 1) C4305

> '*상황에 맞는*':에서 잘림 '*type1*'to'*type2*'

## <a name="remarks"></a>설명

정보의 손실 더 작은 형식 또는 생성자 인수로 초기화에서 값을 변환할 때 경고가 발생 합니다.

## <a name="example"></a>예제

이 샘플에서는 두 가지 방법으로이 경고가 나타날 수 있습니다.

```cpp
// C4305.cpp
// Compile by using: cl /EHsc /W4 C4305.cpp

struct item
{
    item(float) {}
};

int main()
{
    float f = 2.71828;          // C4305 'initializing'
    item i(3.14159);            // C4305 'argument'
    return static_cast<int>(f);
}
```

이 문제를 해결 하려면 올바른 형식의 값을 사용 하 여 초기화 하거나 올바른 형식으로 명시적 캐스트를 사용 합니다. 사용 예를 들어를 **float** 2.71828f 대신 같은 리터럴를 **double** (부동 소수점 리터럴에 대 한 기본 형식)를 초기화를 **float** 변수 또는 전달할를 사용 하는 생성자는 **float** 인수입니다.
