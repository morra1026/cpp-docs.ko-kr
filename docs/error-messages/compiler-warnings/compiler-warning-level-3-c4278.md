---
title: 컴파일러 경고 (수준 3) C4278 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4278
dev_langs:
- C++
helpviewer_keywords:
- C4278
ms.assetid: 4b6053fb-df62-4c04-b6c8-c011759557b8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f63337de2e14b1cb0f9d854df962ab2aa9c8014e
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43205783"
---
# <a name="compiler-warning-level-3-c4278"></a>컴파일러 경고(수준 3) C4278

> '*식별자*': 형식 라이브러리의 식별자 '*tlb*'가 이미 매크로 'rename' 한정자를 사용 하십시오.

사용 하는 경우 [#import](../../preprocessor/hash-import-directive-cpp.md)에 가져오는 typelib에 들어 있는 식별자는 식별자를 선언 하려고 *식별자*합니다. 그러나 이것이 이미 올바른 기호입니다.

사용 된 `#import` **이름 바꾸기** 기호 형식 라이브러리에 별칭을 지정 하는 특성입니다.