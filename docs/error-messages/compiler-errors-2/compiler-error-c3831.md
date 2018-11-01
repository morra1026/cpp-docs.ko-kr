---
title: 컴파일러 오류 C3831
ms.date: 11/04/2016
f1_keywords:
- C3831
helpviewer_keywords:
- C3831
ms.assetid: a125d8dc-b75a-4ea0-b6c7-fe7b119dba25
ms.openlocfilehash: f85f94afa796f4ccf0efecd8f9223c2c48ca623d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50508838"
---
# <a name="compiler-error-c3831"></a>컴파일러 오류 C3831

'member': 'class' 고정 된 데이터 멤버 또는 고정 포인터를 반환 하는 멤버 함수를 사용할 수 없습니다

[pin_ptr (C + + /cli CLI)](../../windows/pin-ptr-cpp-cli.md) 잘못 사용 했습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3831 오류가 생성 됩니다.

```
// C3831a.cpp
// compile with: /clr
ref class Y
{
public:
   int i;
};

ref class X
{
   pin_ptr<int> mbr_Y;   // C3831
   int^ mbr_Y2;   // OK
};

int main() {
   Y y;
   pin_ptr<int> p = &y.i;
}
```
