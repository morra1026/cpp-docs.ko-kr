---
title: 심각한 오류 C1197 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1197
dev_langs:
- C++
helpviewer_keywords:
- C1197
ms.assetid: 22b801b7-e792-41f6-a461-973c03c69f25
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 58561e7bd906fc750779ef53a4f68ec27088a3b7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46024764"
---
# <a name="fatal-error-c1197"></a>심각한 오류 C1197

프로그램에 이미 'mscorlib.dll_2'를 참조 하는 대로 'mscorlib.dll_1'를 참조할 수 없습니다.

컴파일러는 공용 언어 런타임의 버전으로 일치 됩니다.  그러나 시도가 이전 버전에서 공용 언어 런타임 파일의 버전을 참조 하려고 합니다.

이 오류를 해결 하려면만 사용 하 여 컴파일하는 Visual c + +의 버전과 함께 제공 되는 공용 언어 런타임의 버전에서 파일을 참조 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C1197 오류가 생성 됩니다.

```
// C1197.cpp
// compile with: /clr /c
// processor: x86
#using "C:\Windows\Microsoft.NET\Framework\v1.1.4322\mscorlib.dll"   // C1197
// try the following line instead
// #using "mscorlib.dll"
```