---
title: 컴파일러 경고 (수준 4) C4295 | Microsoft Docs
ms.custom: ''
ms.date: 1/09/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4295
dev_langs:
- C++
helpviewer_keywords:
- C4295
ms.assetid: 20dbff85-9f62-4ca3-8fe9-079d4512006d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 63c7a6b640039f6e3008cab924c9d58dfcb1fcc8
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50080613"
---
# <a name="compiler-warning-level-4-c4295"></a>컴파일러 경고(수준 4) C4295

> '*배열*': 배열이 너무 작아서 null 종결 문자를 포함 합니다.

배열 초기화 되었지만 배열에서 마지막 문자를 null 아닙니다. 문자열 배열에 액세스 하면 예기치 않은 결과가 발생할 수 있습니다.

## <a name="example"></a>예제

다음 샘플 C4295를 생성합니다. 이 문제를 해결 하려면 선언할 수 있습니다 배열 크기를 저장할 더 큰 이니셜라이저 문자열에서 종결 null 배열을이 의도 암호화 되도록 배열 이니셜라이저 목록을 사용할 수 `char`, null 종료 문자열이 아닙니다.

```C
// C4295.c
// compile with: /W4

int main() {
   char a[3] = "abc";           // C4295
   char b[3] = {'d', 'e', 'f'}; // No warning
   a[0] = b[2];
}
```
