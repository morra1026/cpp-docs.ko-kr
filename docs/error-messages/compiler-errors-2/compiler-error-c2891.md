---
title: 컴파일러 오류 C2891 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2891
dev_langs:
- C++
helpviewer_keywords:
- C2891
ms.assetid: e12cfb2d-df45-4b0d-b155-c51d17e812fa
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 86d81662cb02fa3c8f6af75009daf4dab9b70196
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016561"
---
# <a name="compiler-error-c2891"></a>컴파일러 오류 C2891

'parameter': 템플릿 매개 변수의 주소를 가져올 수 없습니다.

lvalue가 아닌 경우에 템플릿 매개 변수의 주소를 사용할 수 없습니다. 형식 매개 변수 주소가 없기 때문에 lvalue 않습니다. Lvalue 없는 템플릿 매개 변수 목록에 비형식 값도 수행 주소가 없습니다. 템플릿 매개 변수로 전달 된 값은 템플릿 인수 컴파일러에서 생성 된 복사본 이므로 이것이 컴파일러 오류 C2891 발생 하는 코드의 예입니다.

```
template <int i> int* f() { return &i; }
```

참조 형식과 같이 lvalue는 템플릿 매개 변수 수 주소로 수행 합니다.

```
template <int& r> int* f() { return &r; }
```

이 오류를 해결 하려면 lvalue 경우가 템플릿 매개 변수의 주소를 사용 하지 않습니다.