---
title: 부동 소수점 보조 프로세서 및 호출 규칙 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- floating-point numbers [C++]
- floating-point coprocessor
ms.assetid: 3cc6615a-b308-4cf7-9570-83e192a832b3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e9f45f73e3cb1910bfc604c8a0fde871cef973a9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075958"
---
# <a name="floating-point-coprocessor-and-calling-conventions"></a>부동 소수점 보조 프로세서 및 호출 규칙

를 작성 하는 어셈블리 루틴은 부동 소수점 보조 프로세서 부동 유지 해야 하면 소수점 제어 단어 및 반환 하는 경우가 아니면 보조 프로세서 스택을 정리를 **부동 소수점** 하거나 **double** 값 (함수가 ST(0)에 반환 해야 합니다.

## <a name="see-also"></a>참고자료

[호출 규칙](../cpp/calling-conventions.md)