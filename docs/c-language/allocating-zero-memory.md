---
title: 0 메모리 할당 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- memory allocation, zero memory
- zero memory
ms.assetid: 768f2ab9-83a1-4887-8eb5-c094c18489a8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: bc3b7a92cdc8a05c73f15c7cea917d86a3b6bb46
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085058"
---
# <a name="allocating-zero-memory"></a>0 메모리 할당

**ANSI 4.10.3** 요청된 크기가 0인 경우 `calloc`, `malloc` 또는 `realloc` 함수의 동작

`calloc`, `malloc` 및 `realloc` 함수는 0을 인수로 수락합니다. 실제 메모리가 할당되지는 않지만 유효한 포인터가 반환되고 이후에 realloc을 사용하여 메모리 블록을 수정할 수 있습니다.

## <a name="see-also"></a>참고 항목

[라이브러리 함수](../c-language/library-functions.md)