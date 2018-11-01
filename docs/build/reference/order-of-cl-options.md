---
title: CL 옵션 순서
ms.date: 11/04/2016
f1_keywords:
- cl
helpviewer_keywords:
- cl.exe compiler, setting options
ms.assetid: 300908ce-ae00-4b45-964b-e4e69ff6777b
ms.openlocfilehash: e5dd07f52f853b17bf663e2fbad7dbe66a3a1db7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633537"
---
# <a name="order-of-cl-options"></a>CL 옵션 순서

옵션은 CL 명령줄에서 마지막으로 발생 해야 하는 /link 옵션을 제외 하 고 어디서 나 나타날 수 있습니다. 컴파일러에 지정 된 옵션을 사용 하 여 시작 합니다 [CL 환경 변수](../../build/reference/cl-environment-variables.md) 다음 명령줄을 왼쪽에서 오른쪽으로 읽는 및-명령 파일을 발견 하면 순서 대로 처리 합니다. 각 옵션은 명령줄에서 모든 파일에 적용 됩니다. CL 옵션은 서로 충돌을 발생 하는 경우 오른쪽에 있는 옵션을 사용 합니다.

## <a name="see-also"></a>참고 항목

[컴파일러 명령줄 구문](../../build/reference/compiler-command-line-syntax.md)