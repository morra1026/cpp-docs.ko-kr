---
title: 명령줄 경고 D9026 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- D9026
dev_langs:
- C++
helpviewer_keywords:
- D9026
ms.assetid: 149fe5e3-5329-4be8-b871-49dfd423aaba
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 07be633e56dad6c8f0b304a3c88c1b9919221d4a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46079156"
---
# <a name="command-line-warning-d9026"></a>명령줄 경고 D9026

옵션이 전체 명령줄에 적용

파일 이름 지정 된 명령에는 옵션이 지정 되었습니다. 옵션은 파일 앞에 오는 것에 적용 되었습니다.

예를 들어, 명령에서

```
CL verdi.c /G5 puccini.c
```

사용/g5, / g4 기본값이 아닌 VERDI.c 파일은 컴파일됩니다.

이 동작은 VERDI.c 생성 파일 이름 앞에 지정 된 옵션을 사용 하 여 컴파일할 / G4 및 PUCCINI.c/g5를 사용 하 여 컴파일 중인를 적용 하는 일부 이전 버전의 다릅니다.