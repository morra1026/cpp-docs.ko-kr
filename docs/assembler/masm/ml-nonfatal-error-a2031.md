---
title: ML 심각 하지 않은 오류 A2031 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A2031
dev_langs:
- C++
helpviewer_keywords:
- A2031
ms.assetid: d5b11f58-4a00-42be-9062-8fa8728e6306
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bf6744224847e114e76df6e7ad6470696d3e8387
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43682660"
---
# <a name="ml-nonfatal-error-a2031"></a>ML 심각하지 않은 오류 A2031

**인덱스 또는 기본 등록 해야 합니다.**

메모리 식에 기본 또는 인덱스 레지스터 없는 레지스터를 사용 하려고 했습니다.

예를 들어 다음 식은이 오류가 발생합니다.

```asm
[ax]
[bl]
```

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>