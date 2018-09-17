---
title: CL 옵션 순서 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- cl
dev_langs:
- C++
helpviewer_keywords:
- cl.exe compiler, setting options
ms.assetid: 300908ce-ae00-4b45-964b-e4e69ff6777b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3ffe9a440396df14823775db335e52bca6cacdb3
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725025"
---
# <a name="order-of-cl-options"></a>CL 옵션 순서

옵션은 CL 명령줄에서 마지막으로 발생 해야 하는 /link 옵션을 제외 하 고 어디서 나 나타날 수 있습니다. 컴파일러에 지정 된 옵션을 사용 하 여 시작 합니다 [CL 환경 변수](../../build/reference/cl-environment-variables.md) 다음 명령줄을 왼쪽에서 오른쪽으로 읽는 및-명령 파일을 발견 하면 순서 대로 처리 합니다. 각 옵션은 명령줄에서 모든 파일에 적용 됩니다. CL 옵션은 서로 충돌을 발생 하는 경우 오른쪽에 있는 옵션을 사용 합니다.

## <a name="see-also"></a>참고 항목

[컴파일러 명령줄 구문](../../build/reference/compiler-command-line-syntax.md)