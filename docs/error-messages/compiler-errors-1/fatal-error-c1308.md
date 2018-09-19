---
title: 심각한 오류 C1308 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1308
dev_langs:
- C++
helpviewer_keywords:
- C1308
ms.assetid: 46177997-069e-433a-8e20-93c846d78ffd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dd778e95f3ace413dbeb409da3c4b2493208e8bf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46104188"
---
# <a name="fatal-error-c1308"></a>심각한 오류 C1308

어셈블리를 연결할 수 없습니다.

.netmodule을 링커에 대한 입력 파일로 사용할 수 있지만 어셈블리는 사용할 수 없습니다. 로 컴파일된 어셈블리를 연결 하려고 시도 하는 경우이 오류를 생성할 수 있습니다 `/clr:safe`합니다.

자세한 내용은 [링커 입력 파일로 사용하는 .netmodule 파일](../../build/reference/netmodule-files-as-linker-input.md)을 참조하세요.

다음 샘플에서는 C1308를 생성합니다.

```
// C1308.cpp
// compile with: /clr:safe /LD
public ref class MyClass {
public:
   int i;
};
```

그런 다음

```
// C1308b.cpp
// compile with: /clr /link C1308b.obj C1308.dll
// C1308 expected
#using "C1308.dll"
int main() {
   MyClass ^ my = gcnew MyClass();
}
```