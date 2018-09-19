---
title: 컴파일러 경고 C4687 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4687
dev_langs:
- C++
helpviewer_keywords:
- C4687
ms.assetid: 2f28e0b1-7358-4c88-bd70-aad8f0aa004c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9d813ce6d666431cfc3f74d1409012a4a0aec897
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118715"
---
# <a name="compiler-warning-c4687"></a>컴파일러 경고 C4687

'class': 봉인된 추상 클래스는 'interface' 인터페이스를 구현할 수 없습니다

봉인 된 추상 형식은 일반적으로 정적 멤버 함수를 유지 하는 데만 합니다.

자세한 내용은 [추상](../../windows/abstract-cpp-component-extensions.md)하 고 [봉인](../../windows/sealed-cpp-component-extensions.md)합니다.

기본적으로 C4687 오류로 발생 합니다. C4687 표시 하지 않을 수 있습니다 합니다 [경고](../../preprocessor/warning.md) pragma입니다. 인 경우 추상, 봉인 된 형식에서 인터페이스를 구현 하려는 특정 C4687 억제할 수 있습니다.

## <a name="example"></a>예제

다음 샘플 C4687를 생성합니다.

```
// C4687.cpp
// compile with: /clr /c
interface class A {};

ref struct B sealed abstract : A {};   // C4687
ref struct C sealed : A {};   // OK
ref struct D abstract : A {};   // OK
```