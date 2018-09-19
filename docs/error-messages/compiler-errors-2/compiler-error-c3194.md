---
title: 컴파일러 오류 C3194 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3194
dev_langs:
- C++
helpviewer_keywords:
- C3194
ms.assetid: 49d3ffc6-eff6-4b46-865b-18811692a8bb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 923e4d5535a1be4f4c8a3f7b60730eb6a656ac33
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46077102"
---
# <a name="compiler-error-c3194"></a>컴파일러 오류 C3194

'member': 값 형식 할당 연산자를 사용할 수 없습니다

복사 생성자 또는 복사 할당 연산자와 같은 컴파일러에 의해 자동 호출을 필요로 하는 특수 멤버 함수는 값 클래스 내에서 지원 되지 않습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3194 오류가 발생 합니다.

```
// C3194.cpp
// compile with: /clr /c
value struct MyStruct {
   MyStruct& operator= (const MyStruct& i) { return *this; }   // C3194
};

ref struct MyStruct2 {
   MyStruct2% operator= (const MyStruct2% i) { return *this; }   // OK
};
```