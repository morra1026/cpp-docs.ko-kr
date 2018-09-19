---
title: 컴파일러 경고 (수준 1) C4129 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4129
dev_langs:
- C++
helpviewer_keywords:
- C4129
ms.assetid: a4190c64-4bfb-48fd-8e98-52720bc0d878
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6e02f38044180c45e221099d2874b7f8ff48d62f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46098448"
---
# <a name="compiler-warning-level-1-c4129"></a>컴파일러 경고 (수준 1) C4129

'character': 문자 이스케이프 시퀀스를 인식할 수 없는

합니다 `character` 백슬래시 다음 (\\) 문자 또는 문자열 상수는 유효한 이스케이프 시퀀스도 인식 되지 않습니다. 백슬래시는 무시 되 고 인쇄 되지 않습니다. 백슬래시 다음의 문자가 출력 됩니다.

단일 백슬래시를 인쇄 하려면 이중 백슬래시를 지정 합니다 (\\\\).

C + + 표준, 섹션 2.13.2 이스케이프 시퀀스를 설명합니다.

다음 샘플에서는 C4129 오류가 생성 됩니다.

```
// C4129.cpp
// compile with: /W1
int main() {
   char array1[] = "\/709";   // C4129
   char array2[] = "\n709";   // OK
}
```