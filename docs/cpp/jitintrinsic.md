---
title: jitintrinsic | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- jitintrinsic
- jitintrinsic_cpp
dev_langs:
- C++
helpviewer_keywords:
- __declspec keyword [C++], jitintrinsic
- jitintrinsic __declspec modifier
ms.assetid: 23dbe416-7ef6-442b-b16d-9a81aab04fa6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 888ec19eaedf881fed97a14a7f3f8b5ee673ce7a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056289"
---
# <a name="jitintrinsic"></a>jitintrinsic

64비트 공용 언어 런타임에 중요한 항목으로 함수를 표시합니다. 이는 Microsoft에서 제공하는 라이브러리의 특정 함수에서 사용됩니다.

## <a name="syntax"></a>구문

```
__declspec(jitintrinsic)
```

## <a name="remarks"></a>설명

**jitintrinsic** 추가 MODOPT (<xref:System.Runtime.CompilerServices.IsJitIntrinsic>)를 함수 서명에 합니다.

사용자가이 사용 하 여 권장 되지 않습니다 **__declspec** 한정자, 예기치 않은 결과가 발생할 수 있습니다.

## <a name="see-also"></a>참고자료

[__declspec](../cpp/declspec.md)<br/>
[키워드](../cpp/keywords-cpp.md)