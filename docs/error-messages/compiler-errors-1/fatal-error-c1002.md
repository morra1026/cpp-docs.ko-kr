---
title: 심각한 오류 C1002 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1002
dev_langs:
- C++
helpviewer_keywords:
- C1002
ms.assetid: bd6d274a-c7b4-43af-8bf2-23c5e442aa22
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 82f08255484b11f9f5d87fb67ac8ac7b401d4f6e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46044147"
---
# <a name="fatal-error-c1002"></a>심각한 오류 C1002

2번 패스에서 컴파일러의 힙 공간이 부족합니다.

컴파일러가 너무 많은 기호 또는 복잡 한 식을 사용 하 여 프로그램 되었기 때문일 수 있습니다 하는 두 번째 단계 동적 메모리 공간이 부족합니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 여러 개의 작은 파일을 소스 파일을 나눕니다.

1. 좀 더 작은 하위 식을 나눕니다.

1. 다른 프로그램 또는 메모리를 사용 하는 드라이버를 제거 합니다.