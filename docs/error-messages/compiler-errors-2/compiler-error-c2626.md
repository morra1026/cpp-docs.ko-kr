---
title: 컴파일러 오류 C2626 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2626
dev_langs:
- C++
helpviewer_keywords:
- C2626
ms.assetid: 4c283ad0-251b-4571-bc18-468b9836746f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9929da1f0cf9ffd9c70048017fdef1d854c1fcc9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074684"
---
# <a name="compiler-error-c2626"></a>컴파일러 오류 C2626

'identifier': 익명 구조체 또는 공용 구조체에서는 전용 또는 보호된 데이터 멤버가 허용되지 않습니다.

익명 구조체 또는 공용 구조체의 멤버는 공용 액세스 권한이 있어야 합니다.

다음 샘플에서는 C2626을 생성합니다.

```
// C2626.cpp
int main() {
   union {
   protected:
      int j;     // C2626, j is protected
   private:
      int k;     // C2626, k is private
   };
}
```

이 문제를 해결하려면 전용 또는 보호된 태그를 제거하세요.

```
// C2626b.cpp
int main() {
   union {
   public:
      int i;   // OK, i is public
   };
}
```