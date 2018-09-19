---
title: 컴파일러 오류 C2569 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2569
dev_langs:
- C++
helpviewer_keywords:
- C2569
ms.assetid: 092bed1e-f631-436c-9586-7750629f6fac
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9309576439a772427c6adcb6f94826a8f9230058
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078857"
---
# <a name="compiler-error-c2569"></a>컴파일러 오류 C2569

'EnumOrUnion': 열거형/공용 구조체를 기본 클래스로 사용할 수 없습니다

형식으로 지정 된 공용 구조체 또는 열거형에서 파생 되어야 하는 경우 클래스 또는 구조체에는 공용 구조체 또는 열거형을 변경 합니다.

다음 샘플에서는 C2569 오류가 생성 됩니다.

```
// C2569.cpp
// compile with: /c
union ubase {};
class cHasPubUBase : public ubase {};   // C2569
// OK
struct sbase {};
class cHasPubUBase : public sbase {};
```