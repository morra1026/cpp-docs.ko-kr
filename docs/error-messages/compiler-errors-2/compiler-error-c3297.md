---
title: 컴파일러 오류 C3297 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3297
dev_langs:
- C++
helpviewer_keywords:
- C3297
ms.assetid: 2a718b4c-6cdb-4418-92c0-fc3a259431c4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7aa23cebc7ad7019c375c351f723b7ad1573ab86
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46069837"
---
# <a name="compiler-error-c3297"></a>컴파일러 오류 C3297

'constraint_2': 'constraint_1'에 값 제약 조건이 있으므로 'constraint_1'을 제약 조건으로 사용할 수 없습니다.

값 클래스가 봉인되어 있습니다. 제약 조건이 값 클래스인 경우 다른 제약 조건이 파생될 수 없습니다.

자세한 내용은 [제네릭 형식 매개 변수에 대 한 제약 조건 (C + + CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3297을 생성합니다.

```
// C3297.cpp
// compile with: /clr /c
generic<class T, class U>
where T : value class
where U : T   // C3297
public ref struct R {};
```