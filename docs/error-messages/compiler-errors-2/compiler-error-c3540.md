---
title: 컴파일러 오류 C3540
ms.date: 11/04/2016
f1_keywords:
- C3540
helpviewer_keywords:
- C3540
ms.assetid: 3c0c959c-e3b7-40eb-b922-ccac44bd9d85
ms.openlocfilehash: d0c4f1b71ccd12ad39fb25ef3411d2fb46b89da7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50665818"
---
# <a name="compiler-error-c3540"></a>컴파일러 오류 C3540

'type': 'auto'를 포함 하는 형식에 sizeof를 적용할 수 없습니다

합니다 [sizeof](../../cpp/sizeof-operator.md) 있기 때문에 연산자를 지정된 된 형식에 적용할 수 없습니다는 `auto` 지정자입니다.

## <a name="example"></a>예제

다음 예제에서는 C3540를 생성합니다.

```
// C3540.cpp
// Compile with /Zc:auto
int main() {
    auto x = 123;
    sizeof(x);    // OK
    sizeof(auto); // C3540
    return 0;
}
```

## <a name="see-also"></a>참고 항목

[auto 키워드](../../cpp/auto-keyword.md)<br/>
[/Zc:auto(변수 형식 추론)](../../build/reference/zc-auto-deduce-variable-type.md)<br/>
[sizeof 연산자](../../cpp/sizeof-operator.md)