---
title: 컴파일러 경고 (수준 1) C4153 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4153
dev_langs:
- C++
helpviewer_keywords:
- C4153
ms.assetid: 37a15754-9dba-470b-adda-c4b888064b3e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 99aa207c550004eee1db906acf5dc567e9859f7c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074086"
---
# <a name="compiler-warning-level-1-c4153"></a>컴파일러 경고(수준 1) C4153

식에서 함수/데이터 포인터 변환이 있습니다.

함수 포인터가 데이터 포인터로 변환되거나 그 반대로 변환됩니다. 이 변환은 Microsoft 확장(/Ze)에서는 허용되지만 ANSI C에서는 허용되지 않습니다.