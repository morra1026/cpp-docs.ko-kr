---
title: 컴파일러 경고 (수준 1) C4182 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4182
dev_langs:
- C++
helpviewer_keywords:
- C4182
ms.assetid: 8970f3c6-e2dd-407e-b2ec-964360eb8b43
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 80c0cdac45238a4734b02d34f4c540c62a2f0c09
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056575"
---
# <a name="compiler-warning-level-1-c4182"></a>컴파일러 경고(수준 1) C4182

\#포함 중첩 수준은 'number' 심층; 무한 재귀가 발생할 수 있습니다

중첩된 포함 파일의 수로 인해 힙의 공간이 부족합니다. 다른 포함 파일에 포함된 포함 파일이 중첩됩니다.

이 메시지는 정보 제공을 위해 제공되며 [C1076](../../error-messages/compiler-errors-1/fatal-error-c1076.md)오류를 생성합니다.