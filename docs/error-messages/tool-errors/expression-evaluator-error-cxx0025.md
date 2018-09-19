---
title: 식 계산기 오류 CXX0025 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0025
dev_langs:
- C++
helpviewer_keywords:
- CAN0025
- CXX0025
ms.assetid: 3e2fb541-63b3-46ac-9f93-3dadb253bcf6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dd89faa4de7b296d6a6771f857f3d16dbe2f94f2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043705"
---
# <a name="expression-evaluator-error-cxx0025"></a>식 계산기 오류 CXX0025

연산자에는 구조체/공용 구조체가 필요합니다.

식을 사용 하는 연산자 `struct` 또는 **union** 형식이 없는 식을 적용할를 `struct` 또는 **union**합니다.

클래스, 구조체 또는 공용 구조체 변수의 구성 요소는 정규화 된 이름이 있어야 합니다. 전체 사양이 없는 구성 요소를 입력할 수 없습니다.

이 오류는 can0025와 동일 합니다.