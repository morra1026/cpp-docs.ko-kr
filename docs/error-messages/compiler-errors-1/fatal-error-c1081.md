---
title: 심각한 오류 C1081 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1081
dev_langs:
- C++
helpviewer_keywords:
- C1081
ms.assetid: e58adf17-cbe1-4955-a5c7-80622bbba249
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b34f2f19a0bb8770ea9292fef120c415c0fb255a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46060534"
---
# <a name="fatal-error-c1081"></a>심각한 오류 C1081

'symbol': 파일 이름이 너무 깁니다.

파일 경로 길이가 초과 `_MAX_PATH` (STDLIB.h에서 260 자 정의 됨). 파일의 이름을 줄이십시오.

짧은 파일 이름을 사용 하 여 CL.exe를 호출 하는 경우 컴파일러는 전체 경로 이름을 생성 해야 합니다. 예를 들어 `cl -c myfile.cpp` 생성 하도록 컴파일러에 발생할 수 있습니다.

```
D:\<very-long-directory-path>\myfile.cpp
```