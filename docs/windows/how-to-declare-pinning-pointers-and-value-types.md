---
title: '방법: 고정 포인터 및 값 형식 선언'
ms.date: 10/12/2018
ms.topic: reference
helpviewer_keywords:
- value types, declaring
- pinning pointers
ms.assetid: 57c5ec8a-f85a-48c4-ba8b-a81268bcede0
ms.openlocfilehash: ed7835e3ab6ccda724ccb6c0d7cf5dab8dd4d342
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50660865"
---
# <a name="how-to-declare-pinning-pointers-and-value-types"></a>방법: 고정 포인터 및 값 형식 선언

값 형식은 암시적으로 boxing할 수 있습니다. 자체 및 사용에 다음 값 형식 개체에 대 한 고정 포인터를 선언할 수 있습니다는 **pin_ptr** boxed 값 형식입니다.

## <a name="example"></a>예제

### <a name="code"></a>코드

```cpp
// pin_ptr_value.cpp
// compile with: /clr
value struct V {
   int i;
};

int main() {
   V ^ v = gcnew V;   // imnplicit boxing
   v->i=8;
   System::Console::WriteLine(v->i);
   pin_ptr<V> mv = &*v;
   mv->i = 7;
   System::Console::WriteLine(v->i);
   System::Console::WriteLine(mv->i);
}
```

```Output
8
7
7
```

## <a name="see-also"></a>참고 항목

[pin_ptr(C++/CLI)](../windows/pin-ptr-cpp-cli.md)