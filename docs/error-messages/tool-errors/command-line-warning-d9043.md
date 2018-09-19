---
title: 명령줄 경고 D9043 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- D9043
dev_langs:
- C++
helpviewer_keywords:
- D9043
ms.assetid: 9263e28d-217b-414c-bfb6-86efd3c27a77
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d29371e147c693b2aa49f8dcf838841af3c75c8d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46031875"
---
# <a name="command-line-warning-d9043"></a>명령줄 경고 D9043

'compiler_option';에 대 한 ' warning_level' 값이 잘못 되었습니다 가정 '4999'; 코드 분석 경고가 경고 수준과 연결 되어 있지 않습니다.

## <a name="example"></a>예제

다음 샘플 C9043를 생성합니다.

```
// D9043.cpp
// compile with: /analyze /w16001
// D9043 warning expected
int main() {}
```