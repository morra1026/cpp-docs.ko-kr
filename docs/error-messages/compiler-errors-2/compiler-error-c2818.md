---
title: 컴파일러 오류 C2818
ms.date: 11/04/2016
f1_keywords:
- C2818
helpviewer_keywords:
- C2818
ms.assetid: 715fc7c9-0c6d-452b-b7f5-1682cea5e907
ms.openlocfilehash: f6e33d0e0ee139138df7d8e11357100b3ec3a1a9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50593442"
---
# <a name="compiler-error-c2818"></a>컴파일러 오류 C2818

오버로드된 'operator ->'는 'type' 형식을 통해 재귀적으로 적용됩니다.

재귀를 포함 하는 클래스 멤버 액세스 연산자의 재정의 `return` 문입니다. 다시 정의 하는 `->` 재귀를 사용 하 여 연산자를 이동 해야 재귀 루틴을 별도 함수 호출 연산자에서 함수를 재정의 합니다.