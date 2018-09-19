---
title: 컴파일러 오류 C2431 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2431
dev_langs:
- C++
helpviewer_keywords:
- C2431
ms.assetid: 88a5b648-c89f-47d1-a20e-63231ab4f0f7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 944bead5439abf686fd18e436664e3c1cf7bccb5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049960"
---
# <a name="compiler-error-c2431"></a>컴파일러 오류 C2431

'identifier'에 잘못 된 인덱스 레지스터

ESP 등록을 크기 조정 또는 인덱스와 기본 등록으로 사용 합니다. X86 프로세서 중 하나를 허용 하지 않습니다 인코딩에 형제입니다.

다음 샘플에서는 C2431 오류가 생성 됩니다.

```
// C2431.cpp
// processor: x86
int main() {
   _asm mov ax, [ESI + 2*ESP]   // C2431
   _asm mov ax, [esp + esp]   // C2431
}
```