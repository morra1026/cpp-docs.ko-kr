---
title: 컴파일러 오류 C2722
ms.date: 11/04/2016
f1_keywords:
- C2722
helpviewer_keywords:
- C2722
ms.assetid: 4cc2c7fa-cb12-4bcf-9df1-6d627ef62973
ms.openlocfilehash: 4274ac6ec33e0176f998fcf5a2b3efd570a4009f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50546265"
---
# <a name="compiler-error-c2722"></a>컴파일러 오류 C2722

':: operator': 다음 연산자 명령을; 잘못 되었습니다. 'operator o'를 사용 합니다.

`operator` 문 redefines `::new` 또는 `::delete`합니다. `new` 하 고 `delete` 는 전역 연산자 하므로 범위 결정 연산자 (`::`)은 의미가 없습니다. `::` 연산자를 제거합니다.