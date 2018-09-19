---
title: 컴파일러 오류 C2480 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2480
dev_langs:
- C++
helpviewer_keywords:
- C2480
ms.assetid: 1a58d1c2-971b-4084-96fa-f94aa51c02f1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8b5d8f80293c05b651ad01e725ae501288005dfe
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46102588"
---
# <a name="compiler-error-c2480"></a>컴파일러 오류 C2480

'identifier': 'thread' 정적 범위의 데이터 항목에만 유효.

사용할 수 없습니다는 `thread` 특성을 자동 변수, 비정적 데이터 멤버, 함수 매개 변수 또는 함수 선언 또는 정의 합니다.

사용 된 `thread` 전역 변수, 정적 데이터 멤버 및 정적 변수에 로컬에 대 한 특성입니다.

다음 샘플에서는 C2480를 생성합니다.

```
// C2480.cpp
// compile with: /c
__declspec( thread ) void func();   // C2480
__declspec( thread ) static int i;   // OK
```