---
title: 리소스 컴파일러 심각한 오류 RW1022 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- RW1022
dev_langs:
- C++
helpviewer_keywords:
- RW1022
ms.assetid: 6747c8a9-9c9b-4422-b414-0645d22092d0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: caaefc045a31ca64aa9843927d550ef66285cb2e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099852"
---
# <a name="resource-compiler-fatal-error-rw1022"></a>리소스 컴파일러 심각한 오류 RW1022

**파일 쓰기 I/O 오류**

리소스 컴파일러가 파일에 쓸 수 없습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 디스크 공간이 부족합니다. 사용 가능한 공간을 만들려는 실행 파일의 크기 보다 두 배 이상의 같아야 합니다.

1. 볼륨이 읽기 전용입니다.

1. 불량 섹터입니다.

1. 공유 위반입니다.