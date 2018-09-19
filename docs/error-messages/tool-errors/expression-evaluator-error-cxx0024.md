---
title: 식 계산기 오류 CXX0024 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0024
dev_langs:
- C++
helpviewer_keywords:
- CXX0024
- CAN0024
ms.assetid: eca6adbd-8ff2-4f51-a1cc-a2e9d5d0a47d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2816be7bb1d33757d9722d605d461ac6fb34fadd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118197"
---
# <a name="expression-evaluator-error-cxx0024"></a>식 계산기 오류 CXX0024

작업에 l-value가 필요

L-value를 필요로 하는 작업에 대 한 식에 l-value가 평가 되지 않습니다 지정 되었습니다.

L-value (대입문의 왼쪽에 표시 되기 때문에 이렇게 부름)는 메모리 위치를 참조 하는 식입니다.

예를 들어 `buffer[count]` 유효한 l-value 이므로 특정 메모리 위치를 가리킵니다. 논리 비교 `zed != 0` 메모리 주소 필요가 TRUE 또는 FALSE로 계산 되기 때문에 유효한 l 값이 아닙니다.

이 오류는 can0024와 동일 합니다.