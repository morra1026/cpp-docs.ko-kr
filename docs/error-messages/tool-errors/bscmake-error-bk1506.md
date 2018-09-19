---
title: BSCMAKE 오류 BK1506 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- BK1506
dev_langs:
- C++
helpviewer_keywords:
- BK1506
ms.assetid: f51f8cea-f8fc-4323-bcf2-b7bd119792ee
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 26201a894212701cca19ab2192676b37a69e8b57
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46088698"
---
# <a name="bscmake-error-bk1506"></a>BSCMAKE 오류 BK1506

'filename' 파일을 열 수 없습니다 [: 이유]

BSCMAKE는 파일을 열 수 없습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 다른 프로세스에 의해 잠겨 파일입니다. 하는 경우 `reason` 라는 **사용 권한이 거부 되었습니다**, 브라우저가 파일을 사용 중일 수 있습니다. 찾아보기 창을 닫고 다시 빌드하십시오.

1. 디스크가 꽉 찼습니다.

1. 하드웨어 오류가 발생 합니다.

1. 지정 된 출력 파일 이름이 같은 기존 하위 디렉터리에 있습니다.