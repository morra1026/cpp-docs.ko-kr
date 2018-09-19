---
title: malloc 맞춤 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a8d1d1b4-5122-456f-9a64-a50e105e55a5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: aa6e2748691eeb8a11834bcf8e6962252be7ab3f
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45712064"
---
# <a name="malloc-alignment"></a>malloc 맞춤

[malloc](../c-runtime-library/reference/malloc.md) 에 할당 되는 메모리에 맞출 수 있고 기본 맞춤이 있는 개체를 저장 하도록 적절히 정렬 되는 메모리를 반환 합니다. A *기본 맞춤* 는 맞춤은 맞춤 사양 없이 구현에서 지원 되는 가장 큰 맞춤 보다 작거나 같은입니다. (이것은 맞춤에 대 한 필요한 Visual c + +에서는 `double`, 또는 8 바이트입니다. 64비트 플랫폼을 대상으로 하는 코드에서는 16바이트입니다. 예를 들어, 4 바이트 할당 4 바이트 보다 작은 개체를 지 원하는 경계에 정렬 합니다.

Visual c + +를 갖는 형식이 허용 *확장 된 맞춤*, 라고도 되 *과도 하 게 정렬* 형식입니다. 예를 들어 SSE 형식 [__m128](../cpp/m128.md) 및 `__m256`를 사용 하 여 선언 된 형식과 `__declspec(align( n ))` 여기서 `n` 은 8 보다 큼, 맞춤 확장. 확장 된 맞춤이 필요한 개체에 적합 한 경계에서 메모리 맞춤은 반드시 `malloc`입니다. 사용 과다 정렬 된 형식에 대 한 메모리를 할당할 [_aligned_malloc](../c-runtime-library/reference/aligned-malloc.md) 및 관련 함수입니다.

## <a name="see-also"></a>참고 항목

[스택 사용](../build/stack-usage.md)<br/>
[align](../cpp/align-cpp.md)<br/>
[__declspec](../cpp/declspec.md)