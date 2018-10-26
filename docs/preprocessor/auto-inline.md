---
title: auto_inline | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- auto_inline_CPP
- vc-pragma.auto_inline
dev_langs:
- C++
helpviewer_keywords:
- pragmas, auto_inline
- auto_inline pragma
ms.assetid: f7624cd1-be76-429a-881c-65c9040acf43
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cc2fb4cb870ff1dca2f0b55e9aad20741ffb8220
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50083180"
---
# <a name="autoinline"></a>auto_inline
범위 내에 정의 된 모든 함수를 제외 합니다. 여기서 **해제** 자동 인라인 확장에 대 한 후보로 간주 되 고에서 지정 된 합니다.

## <a name="syntax"></a>구문

```
#pragma auto_inline( [{on | off}] )
```

## <a name="remarks"></a>설명

사용 하는 **auto_inline** pragma를 앞과 바로 뒤 저장 (에 없는) 함수 정의 합니다. pragma가 표시된 후 첫 번째 함수 정의에서 pragma가 적용됩니다.

## <a name="see-also"></a>참고 항목

[Pragma 지시문 및 __Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)