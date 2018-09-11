---
title: Charizing 연산자 (#@) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- '#@'
dev_langs:
- C++
helpviewer_keywords:
- preprocessor, operators
- charizing operator
- '#@ preprocessor operator'
ms.assetid: dee03314-d27c-4063-965c-64756efbef22
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d86c49c8d7d0cda91ba2415167cc79c810a96b3d
ms.sourcegitcommit: d10a2382832373b900b1780e1190ab104175397f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43895307"
---
# <a name="charizing-operator-"></a>Charizing 연산자 (#@)
**Microsoft 전용**

charizing 연산자는 매크로의 인수에만 사용할 수 있습니다. 경우 `#@` 정식 매개 변수 앞에 매크로의 정의에서 실제 인수는 작은따옴표로 묶인 및 매크로 확장 되 면 문자로 처리 합니다. 예를 들어:

```
#define makechar(x)  #@x
```

위의 정의는 다음 문이

```
a = makechar(b);
```

다음과 같이 확장되게 합니다.

```
a = 'b';
```

작은따옴표는 charizing 연산자와 함께 사용할 수 없습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[전처리기 연산자](../preprocessor/preprocessor-operators.md)