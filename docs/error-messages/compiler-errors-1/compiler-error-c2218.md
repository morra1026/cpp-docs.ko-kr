---
title: 컴파일러 오류 C2218 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2218
dev_langs:
- C++
helpviewer_keywords:
- C2218
ms.assetid: b0f55da4-8edb-4b45-b298-1a091981bd7b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 52c449381c6e8a7391706ed6097bc38576bc69fe
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041287"
---
# <a name="compiler-error-c2218"></a>컴파일러 오류 C2218

'__vectorcall'은 '/arch:IA32'와 함께 사용할 수 없습니다.

`__vectorcall` 호출 규칙은 SSE2(스트리밍 SIMD 확장 2) 이상을 포함하는 x86 및 x64 프로세서의 네이티브 코드에서만 지원됩니다. 자세한 내용은 [__vectorcall](../../cpp/vectorcall.md)합니다.

이 오류를 해결하려면 컴파일러 옵션을 대상 SSE2, AVX 또는 AVX2 명령 집합으로 변경합니다. 자세한 내용은 [/arch(x86)](../../build/reference/arch-x86.md)를 참조하세요.