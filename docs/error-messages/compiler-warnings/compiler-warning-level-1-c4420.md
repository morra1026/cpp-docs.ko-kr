---
title: 컴파일러 경고 (수준 1) C4420 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4420
dev_langs:
- C++
helpviewer_keywords:
- C4420
ms.assetid: 44a37754-7ddd-4764-a5f7-d33e05c20091
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e1ba4ef4c4fc006e1a5950d0d16dc530ccc06a1d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049750"
---
# <a name="compiler-warning-level-1-c4420"></a>컴파일러 경고(수준 1) C4420

'operator': '연산자'를 대신 사용 하 여 연산자를 사용할 수 없는 런타임 검사가 손상 될 수 있습니다.

사용 하는 경우이 경고는 발생 합니다 [/RTCv](../../build/reference/rtc-run-time-error-checks.md) (새로운/삭제 확인 vector) 벡터 형식이 없으므로 검색 되 면 및 합니다. 이 경우 비 벡터 형식은 사용 됩니다.

/Rtcv가 제대로 작동 하려면에서 컴파일러는 항상 호출 해야 벡터 형식의 [새](../../cpp/new-operator-cpp.md)/[삭제](../../cpp/delete-operator-cpp.md) 벡터 구문이 사용 된 경우.