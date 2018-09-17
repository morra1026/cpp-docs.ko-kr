---
title: setjmp longjump | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: b0e21902-095d-4198-8f9a-b6326525721a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f53160a5deeb3ea0db111fc0aae7429b19b7cc86
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703276"
---
# <a name="setjmplongjump"></a>setjmp/longjump

Setjmp.h 나 setjmpex.h를 포함 하는 경우 대 한 모든 호출은 [setjmp](../c-runtime-library/reference/setjmp.md) 하거나 [longjmp](../c-runtime-library/reference/longjmp.md) 소멸자를 호출 하 고 마지막으로 호출 하는 해제 됩니다.  이에서 서로 다릅니다 x86, finally 절에 setjmp.h 결과 포함 하 고 소멸자가 호출 되지 않습니다.

에 대 한 호출 `setjmp` 현재 스택 포인터, 비휘발성 레지스터 및 MxCsr 레지스터를 유지 합니다.  에 대 한 호출 `longjmp` 가장 최근의 반환 `setjmp` 호출 스택 포인터, 비휘발성 레지스터 및 MxCsr 레지스터, 상태로 최신으로 유지 되므로 사이트 및 재설정 `setjmp` 호출 합니다.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)