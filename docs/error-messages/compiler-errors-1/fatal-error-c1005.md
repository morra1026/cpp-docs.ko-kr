---
title: 심각한 오류 C1005 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1005
dev_langs:
- C++
helpviewer_keywords:
- C1005
ms.assetid: 150daf8e-a38a-4669-9c1a-a05b5a1f65ef
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 888bdaf2eaddc0d4178affa1ccc4ae77c34f4617
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46092312"
---
# <a name="fatal-error-c1005"></a>심각한 오류 C1005

버퍼에 비해 문자열이 너무 깁니다.

컴파일러 중간 파일의 문자열에서 버퍼를 오버플로했습니다.

[/Fd](../../build/reference/fd-program-database-file-name.md) 또는 [/Yl](../../build/reference/yl-inject-pch-reference-for-debug-library.md) 컴파일러 옵션으로 전달한 매개 변수가 256바이트보다 큰 경우 이 오류가 표시될 수 있습니다.