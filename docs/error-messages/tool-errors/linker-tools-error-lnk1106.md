---
title: 링커 도구 오류 LNK1106 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1106
dev_langs:
- C++
helpviewer_keywords:
- LNK1106
ms.assetid: 528f7e65-04be-4966-b8af-9276837c7cda
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 719ff1a87f3f1afc19cf38736c0059c46a8a9bdc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110876"
---
# <a name="linker-tools-error-lnk1106"></a>링커 도구 오류 LNK1106

잘못 된 파일 또는 전체 디스크: 위치를 찾을 수 없습니다

도구 수를 읽거나 쓸 `location` 메모리 매핑된 파일에 있습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 디스크가 꽉 찼습니다.

     공간을 해제 하 고 다시 연결 합니다.

1. 네트워크를 통해 연결 하려고 합니다.

     일부 네트워크 링커에서 사용 된 메모리 매핑된 파일을 완전히 지원 하지 않습니다. 로컬 디스크에 연결을 시도 합니다.

1. 디스크에 불량 블록입니다.

     운영 체제 및 하드웨어 디스크는는 이러한 오류가 감지, 있지만 디스크 검사 프로그램을 실행 하는 것이 좋습니다.

1. 힙 공간이 부족 합니다.

     참조 [C1060](../../error-messages/compiler-errors-1/fatal-error-c1060.md) 자세한 내용은 합니다.