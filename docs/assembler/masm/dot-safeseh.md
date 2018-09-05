---
title: . SAFESEH | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- .SAFESEH
dev_langs:
- C++
helpviewer_keywords:
- registering functions as exception handlers
- SAFESEH directive
- .SAFESEH directive
ms.assetid: 6eaac8c4-c46f-47ae-8a66-f5cfeb267e43
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d10f3c751fe05c118203bb5eeff6c5cba6ec1c8b
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43693170"
---
# <a name="safeseh"></a>.SAFESEH

구조적된 예외 처리기로 함수를 등록합니다.

## <a name="syntax"></a>구문

> . SAFESEH 식별자

## <a name="remarks"></a>설명

*식별자* 로컬로 정의 대 한 ID 여야 합니다. [PROC](../../assembler/masm/proc.md) 하거나 [EXTRN](../../assembler/masm/extrn.md) 프로시저 A [레이블](../../assembler/masm/label-masm.md) 허용 되지 않습니다. 합니다. SAFESEH 지시문이 필요 합니다 [/safeseh](../../assembler/masm/ml-and-ml64-command-line-reference.md) ml.exe 명령줄 옵션입니다.

구조적된 예외 처리기에 대 한 자세한 내용은 참조 하세요. [/SAFESEH](../../build/reference/safeseh-image-has-safe-exception-handlers.md)합니다.

예를 들어, 안전한 예외 처리기를 등록 하려면 새 MASM 파일 (같이), /safeseh를 사용 하 여 조합 만들고 연결된 된 개체에 추가 합니다.

```asm
.386
.model  flat
MyHandler   proto
.safeseh    MyHandler
end
```

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>