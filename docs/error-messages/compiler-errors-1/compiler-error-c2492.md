---
title: 컴파일러 오류 C2492 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2492
dev_langs:
- C++
helpviewer_keywords:
- C2492
ms.assetid: 8c44c9bb-c366-4fe5-a0ab-882e38608aaa
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2fcb9058bf1aac584e8b7728616f821bda4b33f6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46096277"
---
# <a name="compiler-error-c2492"></a>컴파일러 오류 C2492

'*변수*': 스레드 저장 기간이 있는 데이터는 dll 인터페이스 있을 수 없습니다

사용 하 여 선언 된 변수를 [스레드](../../cpp/thread.md) 특성 및 DLL을 사용 하 여 인터페이스입니다. 주소는 `thread` 변수 까지는 알 수 없는 런타임 DLL 가져오기 또는 내보내기에 연결할 수 없습니다 있도록 합니다.

다음 샘플에서는 C2492 오류가 생성 됩니다.

```
// C2492.cpp
// compile with: /c
class C {
public:
   char   ch;
};

__declspec(dllexport) __declspec(thread) C c_1;   // C2492
__declspec(thread) C c_1;   // OK
```