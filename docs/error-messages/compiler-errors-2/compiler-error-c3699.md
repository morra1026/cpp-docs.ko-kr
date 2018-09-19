---
title: 컴파일러 오류 C3699 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3699
dev_langs:
- C++
helpviewer_keywords:
- C3699
ms.assetid: 47c29afc-ab8b-4238-adfe-788dd6e00b3b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 64e5a5bb98f9e8a6950bbb279c026f167a2ee92e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46107717"
---
# <a name="compiler-error-c3699"></a>컴파일러 오류 C3699

'operator': 'type' 형식에이 간접 참조를 사용할 수 없습니다.

허용 되지 않는 간접 참조를 사용 하려고 `type`합니다.

## <a name="example"></a>예제

다음 샘플 C3699를 생성합니다.

```
// C3699.cpp
// compile with: /clr /c
using namespace System;
int main() {
   String * s;   // C3699
   // try the following line instead
   // String ^ s2;
}
```

## <a name="example"></a>예제

Trivial 속성에 대 한 참조 형식일 수 없습니다. 자세한 내용은 [property](../../windows/property-cpp-component-extensions.md) 를 참조하세요. 다음 샘플 C3699를 생성합니다.

```
// C3699_b.cpp
// compile with: /clr /c
ref struct C {
   property System::String % x;   // C3699
   property System::String ^ y;   // OK
};
```

## <a name="example"></a>예제

"에 대 한 포인터에 대 한 포인터" 구문의 표현은 추적 참조에 대 한 핸들입니다. 다음 샘플 C3699를 생성합니다.

```
// C3699_c.cpp
// compile with: /clr /c
using namespace System;
void Test(String ^^ i);   // C3699
void Test2(String ^% i);
```