---
title: 리소스 컴파일러 심각한 오류 RW1025 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- RW1025
dev_langs:
- C++
helpviewer_keywords:
- RW1025
ms.assetid: 561a02af-e7e0-442a-8ad3-a00b2ca1b62e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2bf7bdeed320c004ffb75fa1d25d9b89147b0c13
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46117402"
---
# <a name="resource-compiler-fatal-error-rw1025"></a>리소스 컴파일러 심각한 오류 RW1025

먼 힙 메모리가 부족 합니다.

너무 많은 공간을 차지 하는 메모리 상주 소프트웨어를 확인 합니다. CHKDSK 프로그램을 사용 하 여 있는 메모리 양을 확인 합니다.

큰 리소스 파일을 만드는 경우 리소스 스크립트 두 파일로 분할 합니다. 두.res 파일을 만든 후 함께 연결 하는 MS-DOS 명령줄을 사용 합니다.

```
copy first.res /b + second.res /b full.res
```