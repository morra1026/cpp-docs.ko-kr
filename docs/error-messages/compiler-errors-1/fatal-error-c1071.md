---
title: 심각한 오류 C1071 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1071
dev_langs:
- C++
helpviewer_keywords:
- C1071
ms.assetid: 489f1786-370e-4ecd-af67-538fe6e5bd4e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1b4487de60148e1da7668bc44c996c5dfb955a9d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46033006"
---
# <a name="fatal-error-c1071"></a>심각한 오류 C1071

주석에서 예기치 않은 파일의 끝이 나타났습니다.

컴파일러는 주석을 검색 하는 동안 파일의 끝에 도달 합니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 주석 종결자 (* /).

1. 소스 파일의 마지막 줄에서 주석 다음 줄 바꿈 문자가 없습니다.

다음 샘플에서는 C1071를 생성합니다.

```
// C1071.cpp
int main() {
}

/* this comment is fine */
/* forgot the closing tag        // C1071
```