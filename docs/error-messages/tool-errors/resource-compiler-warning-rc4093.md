---
title: 리소스 컴파일러 경고 RC4093 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- RC4093
dev_langs:
- C++
helpviewer_keywords:
- RC4093
ms.assetid: 3c61b4a4-b418-465b-a4fd-cb1ff0adb8dd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9b1ca04b17ebdb9d48bc94032482caf48ad4aa00
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46111565"
---
# <a name="resource-compiler-warning-rc4093"></a>리소스 컴파일러 경고 RC4093

비활성 코드의 문자 상수에서 이스케이프 되지 않은 줄 바꿈

상수 식의는 `#if`, `#elif`, **#ifdef**, 또는 **#ifndef** 비활성 전처리기 지시문을 0으로는 코드를 만드는 계산을 따릅니다. 비활성 코드에 내에서 줄 바꿈 문자는 단일 또는 이중 따옴표로 묶어서 표시 되었습니다.

다음 큰따옴표까지 모든 텍스트 문자 상수 내 것으로 간주 되었습니다.