---
title: 링커 도구 오류 LNK1245 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1245
dev_langs:
- C++
helpviewer_keywords:
- LNK1245
ms.assetid: 179c8165-ffbb-44cd-9f24-5250f29577cc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ef7bace5cec937399d7a2ed440e21b9b751f4141
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041794"
---
# <a name="linker-tools-error-lnk1245"></a>링커 도구 오류 LNK1245

잘못 된 하위 시스템 '하위 시스템'; / 하위 시스템은 WINDOWS, WINDOWSCE 또는 CONSOLE 이어야 합니다.

[/clr](../../build/reference/clr-common-language-runtime-compilation.md) 개체를 컴파일하는 데 사용 된 다음 조건 중 하나가 했는데:

- 사용자 지정 진입점이 정의 되었습니다 ([/ENTRY](../../build/reference/entry-entry-point-symbol.md))는 같은 링커 하위 시스템을 유추할 수 없습니다.

- 에 전달 된 값을 [/SUBSYSTEM](../../build/reference/subsystem-specify-subsystem.md) /clr 개체에 대 한 잘못 된 링커 옵션입니다.

두 경우 모두에 대 한 해결 방법을 /SUBSYSTEM 링커 옵션에 유효한 값을 지정 하는 것입니다.