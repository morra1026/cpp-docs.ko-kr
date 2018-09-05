---
title: MMWORD | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- MMWORD
dev_langs:
- C++
helpviewer_keywords:
- MMWORD directive
ms.assetid: b4c5a104-9078-4fb4-afc3-d1e63abe562a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7314c6d0861195e312c7f72481d2e195e041965d
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43679236"
---
# <a name="mmword"></a>MMWORD

MMX와 SSE (XMM) 지침을 사용 하 여 64 비트 멀티미디어 피연산자에 사용 됩니다.

## <a name="syntax"></a>구문

> MMWORD

## <a name="remarks"></a>설명

`MMWORD` 형식이입니다.  MMWORD MASM에 추가 되 고, 이전와 동일한 기능 구현할 수도 있습니다.

```asm
    mov mm0, qword ptr [ebx]
```

64 비트 피연산자에서 두 지침이 작동 하는 동안 `QWORD` 64 비트 부호 없는 정수 형식입니다. 및 `MMWORD` 64 비트 멀티미디어 값의 형식입니다.

`MMWORD` 동일한 형식으로 표시 하기 위해 [__m64](../../cpp/m64.md)합니다.

## <a name="example"></a>예제

```asm
    movq     mm0, mmword ptr [ebx]
```