---
title: 컴파일러 경고(수준 3) C4800
ms.date: 11/04/2016
f1_keywords:
- C4800
helpviewer_keywords:
- C4800
ms.assetid: 4f409799-a250-45ed-bb5f-657691b0d9f7
ms.openlocfilehash: 591b706249201691c7a9743d2cad082eb61e68b5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50636139"
---
# <a name="compiler-warning-level-3-c4800"></a>컴파일러 경고(수준 3) C4800

> '*형식*': bool 'true' 또는 'false' (성능 경고)로 값을 강제 적용

값 없는 경우이 경고가 생성 됩니다 `bool` 할당 되었거나 형식으로 강제 변환할 `bool`합니다. 할당 하 여이 메시지는 발생 하는 일반적으로 `int` 변수를 `bool` 변수 위치는 `int` 변수 값만 포함 **true** 하 고 **false**, 수 형식으로 다시 선언할 `bool`합니다. 형식을 사용 하 여 식을 다시 작성할 수 없습니다 `bool`를 추가 하 여 "`!=0`" 형식을 제공 하는 식과 `bool`합니다. 식 형식으로 캐스팅 `bool` 이 의도적인 경고를 비활성화 하지 않습니다.

이 경고는 Visual Studio 2017에서 더 이상 생성 됩니다.

## <a name="example"></a>예제

다음 샘플 C4800 생성 및이 해결 하는 방법을 보여 줍니다.

```cpp
// C4800.cpp
// compile with: /W3
int main() {
   int i = 0;

   // To fix, instead try:
   // bool i = 0;

   bool j = i;   // C4800
   j++;
}
```