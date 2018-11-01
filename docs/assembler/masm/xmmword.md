---
title: XMMWORD
ms.date: 08/30/2018
f1_keywords:
- XMMWORD
helpviewer_keywords:
- XMMWORD directive
ms.assetid: 18026d32-5cab-403e-ad7e-382fb41aa9b8
ms.openlocfilehash: a248c9318764cd632fed2afd8481ee2b2102fe31
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50479784"
---
# <a name="xmmword"></a>XMMWORD

MMX와 SSE (XMM) 지침을 사용 하 여 128 비트 멀티미디어 피연산자에 사용 됩니다.

## <a name="syntax"></a>구문

> XMMWORD

## <a name="remarks"></a>설명

`XMMWORD` 동일한 형식으로 표시 하기 위해 [__m128](../../cpp/m128.md)합니다.

## <a name="example"></a>예제

```asm
    movdqa   xmm0, xmmword ptr [ebx]
```