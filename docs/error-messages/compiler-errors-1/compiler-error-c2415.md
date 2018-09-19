---
title: 컴파일러 오류 C2415 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2415
dev_langs:
- C++
helpviewer_keywords:
- C2415
ms.assetid: f225c913-2bea-46b1-b096-3d358ac94a15
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bd889880997828396521ddba638bb606552e7d92
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112579"
---
# <a name="compiler-error-c2415"></a>컴파일러 오류 C2415

피연산자 형식이 잘못 되었습니다

Opcode는이 형식의 피연산자를 사용 하지 않습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. Opcode는 사용 된 피연산자의 수를 지원 하지 않습니다. 피연산자의 정확한 수를 결정 하는 어셈블리 언어 참조 설명서를 확인 합니다.

1. 최신 프로세서에는 추가 형식을 사용 하 여 명령을 지원합니다. 조정 된 [/arch (최소 CPU 아키텍처)](../../build/reference/arch-minimum-cpu-architecture.md) 이후 프로세서를 사용할 수 있습니다.