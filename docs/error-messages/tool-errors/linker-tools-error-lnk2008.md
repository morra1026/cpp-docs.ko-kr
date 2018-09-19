---
title: 링커 도구 오류 LNK2008 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK2008
dev_langs:
- C++
helpviewer_keywords:
- LNK2008
ms.assetid: bbcd83c5-c8ae-439e-a033-63643a5bb373
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 18eda06e7f133ada4de1b7ec28ac21be205a71f7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086813"
---
# <a name="linker-tools-error-lnk2008"></a>링커 도구 오류 LNK2008

픽스업 대상이 symbol_name' 맞춤된' 아닙니다.

링크는 픽스업 대상이 제대로 정렬 되지 않은 하는 개체 파일에서 발견 했습니다.

사용자 지정 섹션 맞춤 하 여이 오류를 발생할 수 있습니다 (예를 들어 #pragma [팩](../../preprocessor/pack.md)), [맞춤](../../cpp/align-cpp.md) 한정자 또는 섹션 맞춤을 수정 하는 어셈블리 언어 코드를 사용 하 여 합니다.

코드 위의 사용 하지 않는 경우이 컴파일러에 의해 발생할 수 있습니다.