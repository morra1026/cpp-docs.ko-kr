---
title: 컴파일러 오류 C2432 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2432
dev_langs:
- C++
helpviewer_keywords:
- C2432
ms.assetid: 0e3326e8-cab1-45a5-b48d-61edd33793e8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9ca8c2c62415b6ec3c29c820a23677a87a2695c5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055912"
---
# <a name="compiler-error-c2432"></a>컴파일러 오류 C2432

잘못 된 16 비트 데이터에에서 대 한 'identifier'

16 비트 레지스터 인덱스 또는 기본 등록으로 사용 됩니다. 컴파일러는 16 비트 데이터 참조를 지원 하지 않습니다. 32 비트 코드를 컴파일할 때에 인덱스 또는 기본 등록으로 16 비트 레지스터를 사용할 수 없습니다.

다음 샘플에서는 C2432 오류가 생성 됩니다.

```
// C2432.cpp
// processor: x86
int main() {
   _asm mov eax, DWORD PTR [bx]   // C2432
}
```