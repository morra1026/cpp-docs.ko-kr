---
title: 컴파일러 오류 C2521 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2521
dev_langs:
- C++
helpviewer_keywords:
- C2521
ms.assetid: 6042821b-e345-4a54-a7e9-a2c9019ea016
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 24df0b75d45f9447b26cd8942ff6ca3e751c6a5d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047345"
---
# <a name="compiler-error-c2521"></a>컴파일러 오류 C2521

함수 인수를 사용 하지 않습니다.

소멸자 또는 종료자를 사용 하 여 인수를 사용 하려고 했습니다.

자세한 내용은 [소멸자 및 종료자](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Destructors_and_finalizers)합니다.

## <a name="example"></a>예제

다음 샘플 C2521를 생성합니다.

```
// C2521.cpp
// compile with: /clr
ref class R {
protected:
   !R() {}

public:
   void CleanUp() {
      this->!R(4);   // C2521
      this->!R();   // OK
   }
};

int main() {
   R^ r = gcnew R();
   r->CleanUp();
}
```