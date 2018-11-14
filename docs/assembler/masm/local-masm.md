---
title: LOCAL (MASM)
ms.date: 08/30/2018
f1_keywords:
- Local
helpviewer_keywords:
- LOCAL directive
ms.assetid: 76147e2d-23ca-4f1e-8817-81428becd113
ms.openlocfilehash: 94af498865151ff5c49fac9dbc03de65c4ecb934
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51327605"
---
# <a name="local-masm"></a>LOCAL (MASM)

매크로 내 첫 번째 지시문에서 **로컬** 매크로의 각 인스턴스에 대해 고유한 레이블을 정의 합니다.

## <a name="syntax"></a>구문

> 로컬 *localname* \[하십시오 *localname*]...
>
> 로컬 *레이블을* \[ __\[__ *count*__]__ ] \[ __:__  *형식*] \[ __하십시오__ *레이블* \[ __\[__ *개수* __]__  ] \[ *형식*]]...

## <a name="remarks"></a>설명

프로시저 정의 내에서 두 번째 지시문에서 (**PROC**), **로컬** 절차 중에 존재 하는 스택 기반 변수를 만듭니다. *레이블을* 단순 변수 또는 포함 하는 배열 될 수 있습니다 *개수* 요소입니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>