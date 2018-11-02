---
title: setjmp longjump
ms.date: 11/04/2016
ms.assetid: b0e21902-095d-4198-8f9a-b6326525721a
ms.openlocfilehash: 765cef3f02bed09bed0278aaeecdcdbd55d86b67
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50427900"
---
# <a name="setjmplongjump"></a>setjmp/longjump

Setjmp.h 나 setjmpex.h를 포함 하는 경우 대 한 모든 호출은 [setjmp](../c-runtime-library/reference/setjmp.md) 하거나 [longjmp](../c-runtime-library/reference/longjmp.md) 소멸자를 호출 하 고 마지막으로 호출 하는 해제 됩니다.  이에서 서로 다릅니다 x86, finally 절에 setjmp.h 결과 포함 하 고 소멸자가 호출 되지 않습니다.

에 대 한 호출 `setjmp` 현재 스택 포인터, 비휘발성 레지스터 및 MxCsr 레지스터를 유지 합니다.  에 대 한 호출 `longjmp` 가장 최근의 반환 `setjmp` 호출 스택 포인터, 비휘발성 레지스터 및 MxCsr 레지스터, 상태로 최신으로 유지 되므로 사이트 및 재설정 `setjmp` 호출 합니다.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)