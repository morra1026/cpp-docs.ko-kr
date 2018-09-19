---
title: 컴파일러 오류 C3893 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3893
dev_langs:
- C++
helpviewer_keywords:
- C3893
ms.assetid: 90d52eae-6ef2-4db1-b7ad-92f9e8b140fb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 857d13de61f03bf0784d8cd10ad092d16f7acdaa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087049"
---
# <a name="compiler-error-c3893"></a>컴파일러 오류 C3893

'var': initonly 데이터 멤버의 값 (l-value)-사용 'type_name' 클래스의 인스턴스 생성자 에서만 허용 됩니다

정적 [initonly](../../dotnet/initonly-cpp-cli.md) 데이터 멤버는 정적 생성자의 주소를 하나만 사용할 수 있습니다.

인스턴스 (비정적) initonly 데이터 멤버 인스턴스 (비정적) 생성자의 주소를 하나만 사용할 수 있습니다.

다음 샘플에서는 C3893를 생성합니다.

```
// C3893.cpp
// compile with: /clr
ref struct Y1 {
   Y1() : data_var(0) {
      int% i = data_var;   // OK
   }
   initonly int data_var;
};

int main(){
   Y1^ y= gcnew Y1;
   int% i = y->data_var;   // C3893
}
```