---
title: 컴파일러 오류 C3171 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3171
dev_langs:
- C++
helpviewer_keywords:
- C3171
ms.assetid: 1ce26997-7ef1-4c9f-84da-003ea1a4251e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 32c58f2ecd9651c347f45c29139ffe0ed65a6e3b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082263"
---
# <a name="compiler-error-c3171"></a>컴파일러 오류 C3171

'module': 프로젝트에서 다른 모듈 특성을 지정할 수 없습니다.

[모듈](../../windows/module-cpp.md) 다른 매개 변수 목록 사용 하 여 특성의 두 컴파일에서 파일에서 찾을 수 없습니다. 하나의 고유한 `module` 컴파일 작업당 특성을 지정할 수 있습니다.

동일한 `module` 둘 이상의 소스 코드 파일에서 특성을 지정할 수 있습니다.

예를 들어 경우 다음 `module` 특성이 발견 되었습니다.

```
// C3171.cpp
[ module(name="MyModule", uuid="373a1a4e-469b-11d3-a6b0-00c04f79ae8f", version="1.0") ];
int main() {}
```

그리고

```
// C3171b.cpp
// compile with: C3171.cpp
// C3171 expected
[ module(name="MyModule", uuid="373a1a4e-469b-11d3-a6b0-00c04f79ae8f", version="1.1") ];
```

다르다는 C3171 (다른 버전 값 참고).