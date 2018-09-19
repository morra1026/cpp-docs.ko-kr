---
title: 식 계산기 오류 CXX0016 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0016
dev_langs:
- C++
helpviewer_keywords:
- CAN0016
- CXX0016
ms.assetid: af94a2ae-e835-4da6-8d2f-5c879f72eda2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1e03b0567b77b1ef3f64e5cf98cbe11dab502e1a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075425"
---
# <a name="expression-evaluator-error-cxx0016"></a>식 계산기 오류 CXX0016

상수가 너무 큽니다.

C 식 계산기는 4,294,967,295 (16 진수 0FFFFFFFF) 보다 큰 부호 없는 정수 상수 또는 해당 크기가 약 1.8 e + 308 보다 큽니다. 부동 소수점 상수에 수락할 수 없습니다.

이 오류는 can0016과 동일 합니다.