---
title: 컴파일러 오류 C2708 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2708
dev_langs:
- C++
helpviewer_keywords:
- C2708
ms.assetid: d52d3088-1141-42f4-829c-74755a7fcc3a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c0accd68881cccad5e34530a6c157a4e8179b283
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46111097"
---
# <a name="compiler-error-c2708"></a>컴파일러 오류 C2708

'identifier': 이전 호출 또는 참조와 다른 실제 매개 변수 길이 (바이트)

A [__stdcall](../../cpp/stdcall.md) 함수 프로토타입 뒤에 야 합니다. 이 고, 그렇지 컴파일러 해석 프로토타입으로 함수를 처음으로 호출 하 고 컴파일러와 일치 하지 않는 호출을 발견 하는 경우이 오류가 발생 합니다.

이 오류를 해결 하려면 함수 프로토타입을 추가 합니다.