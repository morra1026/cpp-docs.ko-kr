---
title: 링커 도구 경고 LNK4102 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4102
dev_langs:
- C++
helpviewer_keywords:
- LNK4102
ms.assetid: bfd1b17e-05c7-4bc2-80d6-2888b1a425b2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9daaffc4ddfa9a869c2e60e2c05dc2b7e296d94b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46031865"
---
# <a name="linker-tools-warning-lnk4102"></a>링커 도구 경고 LNK4102

내보내기 삭제 중인 소멸자 'name'; 이미지가 올바르게 실행 되지 않을 수 있습니다.

프로그램 삭제 소멸자 내보내기 하려고 했습니다. 결과 삭제 프로세스를 소유 하지 않은 메모리를 확보할 수 있도록 DLL 경계를 넘어 발생할 수 있습니다. 지정 된 기호는.def 파일에 없는 기호의 인수로 나타나지는 있는지 확인 합니다 **가져오기/** 또는 **/내보내기** 링커 명령줄에 옵션입니다.

C 런타임 라이브러리를 다시 작성 하는 경우에이 메시지를 무시할 수 있습니다.