---
title: 심각한 오류 C1126 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1126
dev_langs:
- C++
helpviewer_keywords:
- C1126
ms.assetid: f22b26a6-8ad7-47cf-a237-196c8ea60aca
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f014aafc60a36bfbb4edad50e7e3ceede6e3c8b2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062477"
---
# <a name="fatal-error-c1126"></a>심각한 오류 C1126

'identifier': 자동 할당 크기를 초과 했습니다.

함수 (및 제한 된 용량의 스왑 가능 함수에 대 한 추가 20 바이트와 같은 컴파일러에 의해 사용 된 공간)의 로컬 변수에 할당 된 공간 제한을 초과 합니다.

이 오류를 해결 하려면 사용 하 여 `malloc` 또는 `new` 많은 양의 데이터를 할당 합니다.