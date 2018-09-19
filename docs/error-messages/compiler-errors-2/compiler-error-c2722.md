---
title: 컴파일러 오류 C2722 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2722
dev_langs:
- C++
helpviewer_keywords:
- C2722
ms.assetid: 4cc2c7fa-cb12-4bcf-9df1-6d627ef62973
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f9138172bb108095c4e72407f1e17e8f4fa2370c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082666"
---
# <a name="compiler-error-c2722"></a>컴파일러 오류 C2722

':: operator': 다음 연산자 명령을; 잘못 되었습니다. 'operator o'를 사용 합니다.

`operator` 문 redefines `::new` 또는 `::delete`합니다. `new` 하 고 `delete` 는 전역 연산자 하므로 범위 결정 연산자 (`::`)은 의미가 없습니다. 제거 된 `::` 연산자입니다.