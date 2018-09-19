---
title: 컴파일러 경고 (수준 3) C4359 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4359
dev_langs:
- C++
helpviewer_keywords:
- C4359
ms.assetid: d8fe993c-ef82-45a0-a43d-c29f9d1bacdb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e97d321b0df8856aadd58f7d27f6339a5776d0f8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46084161"
---
# <a name="compiler-warning-level-3-c4359"></a>컴파일러 경고(수준 3) C4359

'type': 실제 맞춤 (8) __declspec(align()) 지정 된 값 보다 큽니다.

형식에 대해 지정 된 맞춤을 사용 하면 해당 데이터 멤버 중 하나가 형식의 맞춤 보다 작습니다.  자세한 내용은 [맞춤](../../cpp/align-cpp.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4359 오류가 발생 합니다.

```
// C4359.cpp
// compile with: /W3 /c
struct __declspec(align(8)) C8 { __int64 i; };
struct __declspec(align(4)) C4  { C8 m8; };   // C4359
struct __declspec(align(8)) C8_b  { C8 m8; };   // OK
struct __declspec(align(16)) C16  { C8 m8; };   // OK
```