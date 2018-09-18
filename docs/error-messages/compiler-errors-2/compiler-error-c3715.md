---
title: 컴파일러 오류 C3715 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3715
dev_langs:
- C++
helpviewer_keywords:
- C3715
ms.assetid: ee5dce88-ddc4-4bdb-9464-47467ce1674f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 63ae3486b4db21a3aa241d5ebdbbfa0cdc6806f2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026558"
---
# <a name="compiler-error-c3715"></a>컴파일러 오류 C3715

'pointer': 'class'에 대 한 포인터 여야 합니다

에 대 한 포인터를 지정 [__hook](../../cpp/hook.md) 하거나 [__unhook](../../cpp/unhook.md) 올바른 클래스를 가리키지 않았습니다. 이 오류를 해결 하려면 사용자 `__hook` 고 `__unhook` 호출 올바른 클래스에 대 한 포인터를 지정 합니다.