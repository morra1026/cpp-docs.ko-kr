---
title: 컴파일러 오류 C2825 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2825
dev_langs:
- C++
helpviewer_keywords:
- C2825
ms.assetid: c832f1c1-5184-4fc2-9356-12b21daa7af3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1bd0e9f8f2f5444b8835abc9f6802919f0e6c941
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46117584"
---
# <a name="compiler-error-c2825"></a>컴파일러 오류 C2825

var: 클래스 또는 네임 스페이스 뒤에 하는 경우 여야 ': '

실패 한 시도 정규화 된 이름을 하려고 합니다.

예를 들어 코드에 함수 이름을 시작 하는 함수 선언이 포함 되지 않도록 해야:: 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2825 오류가 생성 됩니다.

```
// C2825.cpp
typedef int i;
int main() {
   int* p = new int;
   p->i::i();   // C2825
   // try the following line instead
   // p->i::~i();
}
```