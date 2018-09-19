---
title: 식 계산기 오류 CXX0030 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0030
dev_langs:
- C++
helpviewer_keywords:
- CAN0030
- CXX0030
ms.assetid: ada8b48c-09c8-49bf-ae23-313ed663c4fe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cb2921013d116b7d8f02e1e29380ca3cd14086b9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46102816"
---
# <a name="expression-evaluator-error-cxx0030"></a>식 계산기 오류 CXX0030

식을 계산할 수 없습니다.

기록의 디버거 식 계산기는 식에 대 한 값을 얻지 못했습니다. 가능한 원인 중 하나는 식이 프로그램의 주소 공간 밖에 있는 메모리 참조 (한 가지 예는 null 포인터 역참조). Windows는 프로그램의 주소 공간 밖에 있는 메모리에 대 한 액세스를 허용 하지 않습니다.

식 평가 순서를 제어 하려면 괄호를 사용 하 여 다시 작성할 수도 있습니다.

이 오류는 can0030과 동일 합니다.