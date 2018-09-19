---
title: 컴파일러 경고 (수준 2) C4099 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4099
dev_langs:
- C++
helpviewer_keywords:
- C4099
ms.assetid: 00bb803d-cae7-4ab8-8969-b46f54139ac8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2d7ffee02e8e5414a0e06cc4ba0da77a50c75f53
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110174"
---
# <a name="compiler-warning-level-2-c4099"></a>컴파일러 경고 (수준 2) C4099

'identifier': 'objecttype1' 이제 'objecttype2'를 사용 하 여 표시를 사용 하 여 먼저 표시 하는 형식 이름

구조 선언 된 개체를 클래스로 정의 됩니다 또는 클래스로 선언 된 개체는 구조체가 아니라 정의 됩니다. 컴파일러는 정의에 지정 된 형식을 사용 합니다.

## <a name="example"></a>예제

다음 샘플 C4099를 생성합니다.

```
// C4099.cpp
// compile with: /W2 /c
struct A;
class A {};   // C4099, use different identifer or use same object type
```