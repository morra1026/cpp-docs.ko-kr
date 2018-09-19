---
title: 컴파일러 오류 C3216 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3216
dev_langs:
- C++
helpviewer_keywords:
- C3216
ms.assetid: bbab1efe-8779-4489-8bb0-b11e45f5cbe5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4eb1fb93335dc6fb61e8e73ea11cfc91c6b461b8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043692"
---
# <a name="compiler-error-c3216"></a>컴파일러 오류 C3216

제약 조건은 'type'이 아니라 제네릭 매개 변수여야 합니다.

제약 조건 형식이 잘못되었습니다.

다음 샘플에서는 C3216을 생성합니다.

```
// C3216.cpp
// compile with: /clr
interface struct A {};

generic <class T>
where F : A   // C3216
// Try the following line instead:
// where T : A    // C3216
ref class C {};
```

다음 예제에서는 가능한 해결 방법을 설명합니다.

```
// C3216b.cpp
// compile with: /clr /c
interface struct A {};

generic <class T>
where T : A
ref class C {};
```