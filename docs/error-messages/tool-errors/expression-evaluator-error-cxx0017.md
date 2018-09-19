---
title: 식 계산기 오류 CXX0017 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0017
dev_langs:
- C++
helpviewer_keywords:
- CAN0017
- CXX0017
ms.assetid: af74db02-a64d-49ca-8363-3e044a107580
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 431071137fb3f5b1b276327ee7d21f323ac24c5b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46136246"
---
# <a name="expression-evaluator-error-cxx0017"></a>식 계산기 오류 CXX0017

기호를 찾을 수 없습니다

식에 지정 된 기호를 찾을 수 없습니다.

이 오류의 한 가지 가능한 원인은 기호 이름에 사례 일치 하지 않습니다. C 및 c + +에 대/소문자 구분 언어 이기 때문에 정확한 경우 원본에 정의 된 기호 이름을 지정 합니다.

이 오류는 디버깅 하는 동안 변수를 감시 하기 위해 변수 형식을 캐스팅 하려고 할 때 발생할 수 있습니다. `typedef` 형식에 대 한 새 이름을 선언 하지만 새 형식을 정의 하지 않습니다. 디버거에서 디버거에서 정의 된 형식 이름이 필요 합니다.

이 오류는 can0017과 동일 합니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 기호 사용 되는 위치는 프로그램의 지점에 이미 선언 되어 있는지 확인 합니다.

1. 실제 형식 이름을 사용 하 여 변수를 캐스팅 하 여 디버거에서 아닌 `typedef`-이름을 정의 합니다.