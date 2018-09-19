---
title: 컴파일러 경고 (수준 1) C4276 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4276
dev_langs:
- C++
helpviewer_keywords:
- C4276
ms.assetid: 9d738c2d-29e5-408a-b9ff-be1a850b2238
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 40a6c85b460e9718a8816598afb016e9c7a493b9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46116024"
---
# <a name="compiler-warning-level-1-c4276"></a>컴파일러 경고(수준 1) C4276

'function': 프로토타입을 입력 하지 않았습니다 매개 변수가 없는 것으로 간주

사용 하 여 함수의 주소를 수행 하는 시기를 [__stdcall](../../cpp/stdcall.md) 호출 규칙을 프로토타입을 제공 해야는 컴파일러가 함수의 데코레이팅된 이름을 만들 수 있도록 합니다. 이후 *함수* 컴파일러에 프로토타입이 없는 데코 레이트 된 이름을 만들 때에 함수에 매개 변수가 없는 것으로 가정 합니다.