---
title: 링커 도구 경고 LNK4001 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4001
dev_langs:
- C++
helpviewer_keywords:
- LNK4001
ms.assetid: 0a8b1c3a-64ce-4311-b7c0-065995059246
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f684e85233c4df777a53f03f07936137c425946e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070421"
---
# <a name="linker-tools-warning-lnk4001"></a>링커 도구 경고 LNK4001

지정 된 개체 파일 없음 사용 하는 라이브러리

링커는.lib 파일을 하나 이상 있지만.obj 파일이 전달 되었습니다.

링커를.obj 파일에 액세스할 수는.lib 파일에서 정보에 액세스할 수 없기 때문에이 경고는 명시적으로 다른 링커 옵션을 지정 해야 합니다를 나타냅니다. 지정 해야 하는 예를 들어,를 [/기계](../../build/reference/machine-specify-target-platform.md), [/out](../../build/reference/out-output-file-name.md), 또는 [/ENTRY](../../build/reference/entry-entry-point-symbol.md) 옵션입니다.