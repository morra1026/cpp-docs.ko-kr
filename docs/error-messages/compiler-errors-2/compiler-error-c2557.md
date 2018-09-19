---
title: 컴파일러 오류 C2557 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2557
dev_langs:
- C++
helpviewer_keywords:
- C2557
ms.assetid: 48a33d82-aa16-4658-b346-2311fcb39864
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f975bdacf4db0460f6b12cd4f340c72e50f01a8c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46102608"
---
# <a name="compiler-error-c2557"></a>컴파일러 오류 C2557

'identifier': 전용 및 보호된 멤버는 생성자 없이 초기화할 수 없습니다.

멤버와 friend만 private 또는 protected 멤버에 값을 할당할 수 있습니다. public이 아닌 멤버는 클래스 생성자에서 초기화해야 합니다.