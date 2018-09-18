---
title: 컴파일러 경고 (수준 4) C4207 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4207
dev_langs:
- C++
helpviewer_keywords:
- C4207
ms.assetid: f4e09e3e-ac87-4489-8e3f-c8f76b82e721
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a5aa7f364eb8f60d680dde4c252b9c84e258cda0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068834"
---
# <a name="compiler-warning-level-4-c4207"></a>컴파일러 경고(수준 4) C4207

비표준 확장이 사용 됨: 확장 이니셜라이저 형식

Microsoft 확장명 (/Ze)으로 크기가 지정 되지 않은 배열을 초기화할 수 있습니다 `char` 중괄호 내에 있는 문자열을 사용 합니다.

## <a name="example"></a>예제

```
// C4207.c
// compile with: /W4
char c[] = { 'a', 'b', "cdefg" }; // C4207

int main()
{
}
```

이러한 초기화는 ANSI 호환성 사용할 수 없습니다 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).