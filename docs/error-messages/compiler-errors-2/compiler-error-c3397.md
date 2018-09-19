---
title: 컴파일러 오류 C3397 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3397
dev_langs:
- C++
helpviewer_keywords:
- C3397
ms.assetid: a8536e87-79c4-4ed7-bd96-42704d06391f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 80db76886b4de529b75fd402a70af7c9fa2a892c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064076"
---
# <a name="compiler-error-c3397"></a>컴파일러 오류 C3397

기본 인수에서는 집합체 초기화가 허용되지 않습니다.

배열이 잘못 선언되었습니다.  참조 [배열](../../windows/arrays-cpp-component-extensions.md) 자세한 내용은 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3397을 생성합니다.

```
// C3397.cpp
// compile with: /clr
// /clr /c
void Func(array<int> ^p = gcnew array<int> { 1, 2, 3 });   // C3397
void Func2(array<int> ^p = gcnew array<int> (3));   // OK

int main() {
   array<int> ^p = gcnew array<int> { 1, 2, 3};   // OK
}
```