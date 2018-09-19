---
title: 컴파일러 오류 C2785 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2785
dev_langs:
- C++
helpviewer_keywords:
- C2785
ms.assetid: d8d13360-0d00-4815-8475-b49c7f0dc0f3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cfae8a58d9c42c9ddc3ef7779fc86f7157ba41b0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46080859"
---
# <a name="compiler-error-c2785"></a>컴파일러 오류 C2785

'declaration1' 및 'declaration2'는 다른 반환 형식

기본 함수 템플릿은의 반환 형식에서 함수 템플릿 특수화의 반환 형식이 서로 다릅니다.

### <a name="to-correct-this-error"></a>이 오류를 해결하려면

1. 일관성에 대 한 함수 템플릿의 모든 특수화를 확인 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2785를 생성합니다.

```
// C2785.cpp
// compile with: /c
template<class T> void f(T);

template<> int f(int); // C2785
template<> void f(int); // OK
```