---
title: 컴파일러 오류 C2097 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2097
dev_langs:
- C++
helpviewer_keywords:
- C2097
ms.assetid: 7e5b2fd4-f61c-4b8a-b265-93e987a04bd3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2da955f5382a1ebacdb507a69ed02627b11462e5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46021865"
---
# <a name="compiler-error-c2097"></a>컴파일러 오류 C2097

초기화가 잘못 되었습니다

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 상수가 아닌 값으로 사용 하 여 변수를 초기화 합니다.

1. 긴 주소를 사용 하 여 짧은 주소를 초기화 합니다.

1. 로컬 구조체, 공용 구조체 또는 비상수 식 컴파일할 때 사용 하 여 배열 초기화 **/Za**합니다.

1. 쉼표 연산자를 포함 하는 식으로 초기화 합니다.

1. 이 아니고 기호화 된 상수는 식으로 초기화 합니다.