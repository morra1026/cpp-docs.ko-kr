---
title: 컴파일러 오류 C3101 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3101
dev_langs:
- C++
helpviewer_keywords:
- C3101
ms.assetid: 4f673766-d4f7-4632-94a5-d36a83f7f4b5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 69f881206528d83dc298fd262dd54c1dd84a7308
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049841"
---
# <a name="compiler-error-c3101"></a>컴파일러 오류 C3101

명명 된 특성 인수 'field'에 대 한 식이 잘못 되었습니다.

명명 된 특성 인수를 초기화 하는 경우 값은 컴파일 시간 상수 여야 합니다.

특성에 대 한 자세한 내용은 참조 하세요. [사용자 정의 특성](../../windows/user-defined-attributes-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3101를 생성합니다.

```
// C3101.cpp
// compile with: /clr /c
ref class AAttribute : System::Attribute {
public:
   int Field;
};

extern int i;

[assembly:A(Field = i)];   // C3101
[assembly:A(Field = 0)];   // OK
```