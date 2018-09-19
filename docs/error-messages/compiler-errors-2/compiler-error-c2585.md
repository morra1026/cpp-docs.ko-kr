---
title: 컴파일러 오류 C2585 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2585
dev_langs:
- C++
helpviewer_keywords:
- C2585
ms.assetid: 05bb1a9c-28fb-4a88-a1b5-aea85ebdee1c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7ec7b1e9c1e5e7894740cc80f9c030fa1ee26ec0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46028846"
---
# <a name="compiler-error-c2585"></a>컴파일러 오류 C2585

'type' 명시적 변환이 모호 합니다.

형식을 변환 하 여 둘 이상의 결과 생성할 수 있습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 다중 상속 기반 클래스 또는 구조체 형식에서 변환 합니다. 변환 함수 또는 연산자 형식에서 동일한 기본 클래스를 두 번 이상 상속 하는 경우 범위 결정 사용 해야 합니다 (`::`) 변환에 사용할 상속 된 클래스를 지정 합니다.

1. 변환 연산자와 생성자를 정의한 동일한 변환을 수행 합니다.