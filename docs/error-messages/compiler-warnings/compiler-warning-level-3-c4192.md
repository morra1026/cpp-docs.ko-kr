---
title: 컴파일러 경고 (수준 3) C4192 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4192
dev_langs:
- C++
helpviewer_keywords:
- C4192
ms.assetid: ea5f91fa-8c96-4f3f-ac42-0c8a86d4e5df
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 671a8c83dcadcaa89372e53b6c3d677c5810b4a5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46114412"
---
# <a name="compiler-warning-level-3-c4192"></a>컴파일러 경고 (수준 3) C4192

'name' 형식 라이브러리 'library'를 가져오는 동안 자동으로 제외 합니다.

A `#import` 라이브러리 항목을 포함 *이름*가 Win32 시스템 헤더에도 정의 합니다. 형식 라이브러리의 제한으로 인해 이름이 같은 **IUnknown** 또는 GUID는 종종에 정의 된 형식 라이브러리를 시스템 헤더에서 정의 복제 합니다. `#import` 이러한 항목을 감지 하 고.tlh 및.tli 헤더 파일에 통합 하기를 거부 합니다.

이 동작을 재정의 하려면 사용 하 여 `#import` 특성 [no_auto_exclude](../../preprocessor/no-auto-exclude.md) 하 고 [include ()](../../preprocessor/include-parens.md)합니다.