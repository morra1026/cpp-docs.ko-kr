---
title: 컴파일러 경고 (수준 3) C4240 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4240
dev_langs:
- C++
helpviewer_keywords:
- C4240
ms.assetid: a2657cdb-18e1-493f-882b-4e10c0bca71d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d2f3c059e63bcca9bbde9e863cc17c9e240e4f78
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46057017"
---
# <a name="compiler-warning-level-3-c4240"></a>컴파일러 경고(수준 3) C4240

비표준 확장이 사용 됨: 이제 정의 이전에 ' 액세스 지정자', 'classname'에 대 한 액세스 '액세스 지정자'로 정의 된

ANSI 호환성 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)), 중첩 된 클래스에 대 한 액세스를 변경할 수 없습니다. 기본 Microsoft 확장 (/Ze)에서는 수를이 경고를 사용 하 여.

## <a name="example"></a>예제

```
// C4240.cpp
// compile with: /W3
class X
{
private:
   class N;
public:
   class N
   {   // C4240
   };
};

int main()
{
}
```