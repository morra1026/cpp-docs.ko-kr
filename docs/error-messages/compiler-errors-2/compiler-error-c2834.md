---
title: 컴파일러 오류 C2834 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2834
dev_langs:
- C++
helpviewer_keywords:
- C2834
ms.assetid: 28f9f6eb-ab2a-4e64-aaaa-9d14f955de41
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b94e1a3fba9bc3589af020340651b4546347cf1a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46089348"
---
# <a name="compiler-error-c2834"></a>컴파일러 오류 C2834

'operator o p는 전역적으로 정규화 해야 합니다.

합니다 `new` 및 `delete` 연산자 상주 하는 클래스에 연결 됩니다. 버전을 선택 하려면 범위 확인을 사용할 수 없습니다 `new` 또는 `delete` 다른 클래스에서. 여러 형태의 구현 하는 `new` 또는 `delete` 연산자는 추가 형식 매개 변수를 사용 하 여 연산자의 버전을 만듭니다.