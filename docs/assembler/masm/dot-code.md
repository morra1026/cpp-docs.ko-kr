---
title: . 코드 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- .CODE
dev_langs:
- C++
helpviewer_keywords:
- .CODE directive
ms.assetid: 2b8c882c-c0d2-4fa3-8335-e6b12717a4f4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ff2d66cfc79e84c8c4c7cf92e117c9ac8c84a555
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43682489"
---
# <a name="code"></a>.CODE

와 함께 사용할 경우 [합니다. 모델](../../assembler/masm/dot-model.md), 코드 세그먼트의 시작을 나타냅니다.

## <a name="syntax"></a>구문

> . 코드 [[name]]

#### <a name="parameters"></a>매개 변수

|매개 변수|설명|
|---------------|-----------------|
|`name`|코드 세그먼트의 이름을 지정 하는 선택적 매개 변수입니다. 기본 이름은 작은, 작음, compact 및 플랫 _TEXT [모델](../../assembler/masm/dot-model.md)합니다. 기본 이름은 *modulename*_TEXT 다른 모델에 대 한 합니다.|

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>
[.DATA](../../assembler/masm/dot-data.md)<br/>