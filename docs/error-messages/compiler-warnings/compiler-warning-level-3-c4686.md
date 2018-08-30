---
title: 컴파일러 경고 (수준 3) C4686 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4686
dev_langs:
- C++
helpviewer_keywords:
- C4686
ms.assetid: 767c83c2-9e4b-4f9e-88c8-02128ba563f4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 32a44cd929eb7629ef317ce9847950b613bde52c
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43202082"
---
# <a name="compiler-warning-level-3-c4686"></a>컴파일러 경고(수준 3) C4686

> '*사용자 정의 형식*': 동작 변경 되었을 수 있습니다, udt 반환 호출 규칙이

## <a name="remarks"></a>설명

클래스 템플릿 특수화가 없는 반환 형식에 사용 되기 전에 정의 됩니다. C4686; 확인 되는 클래스를 인스턴스화하는 모든 항목 인스턴스를 선언 하거나 멤버에 액세스 (C\<int >:: 아무 것도) 옵션 이기도 합니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

## <a name="example"></a>예제

대신 다음 사용해 보세요.

```cpp
// C4686.cpp
// compile with: /W3
#pragma warning (default : 4686)
template <class T>
class C;

template <class T>
C<T> f(T);

template <class T>
class C {};

int main() {
   f(1);   // C4686
}

template <class T>
C<T> f(T) {
   return C<int>();
}
```