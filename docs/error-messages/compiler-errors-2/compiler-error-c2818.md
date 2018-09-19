---
title: 컴파일러 오류 C2818 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2818
dev_langs:
- C++
helpviewer_keywords:
- C2818
ms.assetid: 715fc7c9-0c6d-452b-b7f5-1682cea5e907
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f692f52477c988c277f60a689dac5ce83a90acb2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112046"
---
# <a name="compiler-error-c2818"></a>컴파일러 오류 C2818

오버로드된 'operator ->'는 'type' 형식을 통해 재귀적으로 적용됩니다.

재귀를 포함 하는 클래스 멤버 액세스 연산자의 재정의 `return` 문입니다. 다시 정의 하는 `->` 재귀를 사용 하 여 연산자를 이동 해야 재귀 루틴을 별도 함수 호출 연산자에서 함수를 재정의 합니다.