---
title: 컴파일러 오류 C2778 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2778
dev_langs:
- C++
helpviewer_keywords:
- C2778
ms.assetid: b24cb732-2914-42cc-8928-e2d87b393428
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6106832ea82531a6f6915417ac56d53504db882e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022164"
---
# <a name="compiler-error-c2778"></a>컴파일러 오류 C2778

__declspec에서 GUID 형식이 잘못 되었습니다

잘못 된 GUID에 제공 되는 [uuid](../../cpp/uuid-cpp.md) 확장 된 특성입니다.

GUID는 형식은 16 진수 숫자의 문자열 이어야 합니다.

```
// C2778a.cpp
// compile with: /c
struct __declspec(uuid("00000000-0000-0000-0000-000000000000")) A {};
struct __declspec(uuid("{00000000-0000-0000-0000-000000000000}")) B{};
```

합니다 `uuid` 확장 된 특성에서 인식 하는 문자열을 수락 [CLSIDFromString](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromstring)중괄호로 구분 기호 유무, 합니다.

다음 샘플에서는 C2778 오류가 생성 됩니다.

```
// C2778b.cpp
struct __declspec(uuid(" 00000000-0000-0000-0000-000000000000 ")) C { };   // C2778
struct __declspec(uuid("00000000000000000000000000000000")) D { };   // C2778
```