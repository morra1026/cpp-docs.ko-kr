---
title: 컴파일러 오류 C2897 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2897
dev_langs:
- C++
helpviewer_keywords:
- C2897
ms.assetid: a88349e2-823f-42a0-8660-0653b677afa4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2d05663b913a3e310c091b62a81483f28bbf2c09
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049833"
---
# <a name="compiler-error-c2897"></a>컴파일러 오류 C2897

소멸자/종료자는 함수 템플릿일 수 없습니다.

소멸자 또는 종료자 오버 로드할 수 없습니다, 소멸자 (있는 소멸자의 집합을 정의)를 템플릿으로 선언 허용 되지 않습니다.

다음 샘플에서는 C2897를 생성합니다.

## <a name="example"></a>예제

다음 샘플 C2897를 생성합니다.

```
// C2897.cpp
// compile with: /c
class X {
public:
   template<typename T> ~X() {}   // C2897
};
```

## <a name="example"></a>예제

다음 샘플 C2897를 생성합니다.

```
// C2897_b.cpp
// compile with: /c /clr
ref struct R2 {
protected:
   template<typename T> !R2(){}   // C2897 error
};
```