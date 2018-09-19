---
title: 컴파일러 오류 C2856 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2856
dev_langs:
- C++
helpviewer_keywords:
- C2856
ms.assetid: fe616c51-124e-49e3-9dd8-883ec1660680
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: df6226bfd2fc11f05f894091f4ff02c145d09e11
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072719"
---
# <a name="compiler-error-c2856"></a>컴파일러 오류 C2856

\#pragma hdrstop #if 블록 내 여야 합니다.

`hdrstop` 조건부 컴파일 블록의 본문 안에 pragma를 배치할 수 없습니다.

이동 합니다 `#pragma hdrstop` 영역에 포함 되지 않은 문을 `#if/#endif` 블록입니다.