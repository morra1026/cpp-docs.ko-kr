---
title: LOCAL (MASM) | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- Local
dev_langs:
- C++
helpviewer_keywords:
- LOCAL directive
ms.assetid: 76147e2d-23ca-4f1e-8817-81428becd113
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e8105bc8168ce28d468a1378c5cf7889907a7c9f
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43685065"
---
# <a name="local-masm"></a>LOCAL (MASM)

매크로 내 첫 번째 지시문에서 **로컬** 매크로의 각 인스턴스에 대해 고유한 레이블을 정의 합니다.

## <a name="syntax"></a>구문

> 로컬 *localname* [[합니다 *localname*]]...

> 로컬 *레이블을* [[[*개수*]]] [[:*형식*]] [[를 *레이블* [[[*개수*]]] [[ *형식*]]]]...

## <a name="remarks"></a>설명

프로시저 정의 내에서 두 번째 지시문에서 (**PROC**), **로컬** 절차 중에 존재 하는 스택 기반 변수를 만듭니다. *레이블을* 단순 변수 또는 포함 하는 배열 될 수 있습니다 *개수* 요소입니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>