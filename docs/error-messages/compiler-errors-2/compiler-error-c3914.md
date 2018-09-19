---
title: 컴파일러 오류 C3914 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3914
dev_langs:
- C++
helpviewer_keywords:
- C3914
ms.assetid: 8f3190e6-ee50-4916-9ecc-3b8748b2e1e7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7bb10652a6328bb8ddcc3a8e62755a960a7fc850
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029418"
---
# <a name="compiler-error-c3914"></a>컴파일러 오류 C3914

기본 속성은 정적일 수 없습니다.

기본 속성을 잘못 선언 되었습니다.  자세한 내용은 [방법: 사용 하 여 속성 C + + CLI](../../dotnet/how-to-use-properties-in-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3914 생성 및이 해결 하는 방법을 보여 줍니다.

```
// C3914.cpp
// compile with: /clr /c
ref struct X {
   static property int default[int] {   // C3914
   // try the following line instead
   // property int default[int] {
      int get(int) { return 0; }
      void set(int, int) {}
   }
};
```