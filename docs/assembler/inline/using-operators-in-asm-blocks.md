---
title: __Asm 블록에서 연산자 사용 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- brackets [ ]
- brackets [ ], __asm blocks
- __asm keyword [C++], operators
- square brackets [ ], __asm blocks
- operators [C++], using in __asm blocks
- square brackets [ ]
ms.assetid: a26ccfd4-40ae-4a61-952f-c417982aa8dd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8731169013cba50e01c36aa721859e136938f015
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43676912"
---
# <a name="using-operators-in-asm-blocks"></a>__asm 블록에서 연산자 사용

**Microsoft 전용**

`__asm` 블록은 같은 C 또는 c + + 관련 연산자를 사용할 수 없습니다 합니다 **<<** 연산자입니다. 그러나 공유 하는 연산자 C 및 MASM에서 같은 \* 연산자 어셈블리 언어 연산자로 해석 됩니다. 예를 들어, 외부 프로그램 `__asm` 대괄호를 차단 (**[]**) 바깥쪽 C 배열에 있는 요소의 크기를 자동으로 배율을 조정 하는 배열 첨자로 해석 됩니다. `__asm` 블록 안에서 MASM 인덱스 연산자로 표시되며, 이 연산자는 임의의 데이터 개체 또는 레이블(배열만이 아님)로부터 크기를 조절하지 않은 바이트 오프셋을 만듭니다. 다음 코드에서는 차이점을 보여 줍니다.

```cpp
int array[10];

__asm mov array[6], bx ;  Store BX at array+6 (not scaled)

array[6] = 0;         /* Store 0 at array+24 (scaled) */
```

`array`에 대한 첫 번째 참조는 크기가 조정되지 않지만 두 번째 참조는 크기가 조정됩니다. 사용할 수 있는 참고 합니다 **형식** 상수를 기반으로 크기 조절을 하기 위해서 연산자입니다. 예를 들어, 다음 문은 동일합니다.

```cpp
__asm mov array[6 * TYPE int], 0 ; Store 0 at array + 24

array[6] = 0;                   /* Store 0 at array + 24 */
```

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[__asm 블록에서 C 또는 C++ 사용](../../assembler/inline/using-c-or-cpp-in-asm-blocks.md)<br/>