---
title: 식 계산기 오류 CXX0015 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0015
dev_langs:
- C++
helpviewer_keywords:
- CXX0015
- CAN0015
ms.assetid: 35efaf77-d578-48d8-bfc5-fdeb2a46a8b5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1aa37a2cc7208063ce4cfa786de196842ab42b45
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46050818"
---
# <a name="expression-evaluator-error-cxx0015"></a>식 계산기 오류 CXX0015

식이 너무 복잡 합니다. (스택 오버플로)

입력 한 식이 너무 복잡 하거나 C 식 계산기에 제공 된 저장소의 양을 너무 많이 중첩 되었습니다.

오버플로 일반적으로 너무 많은 보류 중인 계산으로 인해 발생합니다.

계산할 식의 다른 부분에 대 한 대기 하는 대신 발견 될 때 식의 각 구성 요소를 계산할 수 있도록 식을 다시 정렬 합니다.

식은 여러 명령을 나눕니다.

이 오류는 can0015와 동일 합니다.