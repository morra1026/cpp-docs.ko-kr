---
title: 컴파일러 오류 C3116 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3116
dev_langs:
- C++
helpviewer_keywords:
- C3116
ms.assetid: 597463e1-a5cc-4ed3-a917-eae9a61d3312
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1104b731fa565991615eb88cc34fa946e2bfb505
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46077850"
---
# <a name="compiler-error-c3116"></a>컴파일러 오류 C3116

'저장소 specifier': 인터페이스 메서드에 대 한 잘못 된 저장소 클래스

사용한 `typedef`, `register`, 또는 `static` 인터페이스 메서드에 대 한 저장소 클래스입니다. 저장소 클래스가 인터페이스 멤버에서 허용 되지 않습니다.

다음 샘플에서는 C3116 오류가 생성 됩니다.

```
// C3116.cpp
__interface ImyInterface
{
   static void myFunc();   // C3116
};
```