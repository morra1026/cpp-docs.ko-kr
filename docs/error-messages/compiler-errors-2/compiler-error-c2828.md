---
title: 컴파일러 오류 C2828 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2828
dev_langs:
- C++
helpviewer_keywords:
- C2828
ms.assetid: d8df6ed4-5954-46c2-b59b-52881d4e923d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 65d9c36946459372924adc23caa5a44c40568f33
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051934"
---
# <a name="compiler-error-c2828"></a>컴파일러 오류 C2828

'operator o p 이진 형식을 사용 하 여 전역으로 재정의할 수 없습니다.

연산자는 개체의 외부에서 이진 형식을 가질 수 없습니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 개체로 로컬 오버 로드 된 연산자를 확인 합니다.

1. 적절 한 단항 연산자 오버 로드를 선택 합니다.