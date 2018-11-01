---
title: 컴파일러 오류 C3880
ms.date: 11/04/2016
f1_keywords:
- C3880
helpviewer_keywords:
- C3880
ms.assetid: b0e05d1e-32d0-4034-9246-f37d23573ea9
ms.openlocfilehash: 60b96a9e704215ec1cbbab63eb77ca5d43ccb627
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626943"
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