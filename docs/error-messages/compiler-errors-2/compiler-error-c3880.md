---
title: 컴파일러 오류 C3880 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3880
dev_langs:
- C++
helpviewer_keywords:
- C3880
ms.assetid: b0e05d1e-32d0-4034-9246-f37d23573ea9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 03cd1c953e4f0183fe71dcbcf4cc3bfb242b4f1c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074359"
---
# <a name="compiler-error-c3880"></a>컴파일러 오류 C3880

'var': 리터럴 데이터 멤버가 될 수 없습니다.

형식의 [리터럴](../../windows/literal-cpp-component-extensions.md) 설정 해야 합니다 또는 컴파일 타임 다음 형식 중 하나로 변환할:

- 정수 계열 형식

- string

- 정수 계열 또는 기본 형식 사용 하 여 열거형

다음 샘플에서는 C3880 오류가 생성 됩니다.

```
// C3880.cpp
// compile with: /clr /c
ref struct Y1 {
   literal System::Decimal staticConst1 = 10;   // C3880
   literal int staticConst2 = 10;   // OK
};
```