---
title: 컴파일러 오류 C3185 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3185
dev_langs:
- C++
helpviewer_keywords:
- C3185
ms.assetid: 5bf96279-043c-4981-9d02-b4550071b192
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fd7f94f86165fdfd25bb5a901cdb4349a0e48494
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46044524"
---
# <a name="compiler-error-c3185"></a>컴파일러 오류 C3185

'typeid' : 관리되는 형식 또는 WinRT 형식 'type'에 사용되었습니다. 대신 'operator'를 사용하세요.

적용할 수 없습니다는 [typeid](../../cpp/typeid-operator.md) 연산자를 관리 되는 또는 WinRT 형식에 사용 하 여 [typeid](../../windows/typeid-cpp-component-extensions.md) 대신 합니다.

다음 샘플에서는 C3185 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C3185a.cpp
// compile with: /clr
ref class Base {};
ref class Derived : public Base {};

int main() {
   Derived ^ pd = gcnew Derived;
   Base ^pb = pd;
   const type_info & t1 = typeid(pb);   // C3185
   System::Type ^ MyType = Base::typeid;   // OK
};
```
