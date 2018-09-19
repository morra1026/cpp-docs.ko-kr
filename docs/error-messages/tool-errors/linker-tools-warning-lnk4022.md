---
title: 링커 도구 경고 LNK4022 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4022
dev_langs:
- C++
helpviewer_keywords:
- LNK4022
ms.assetid: 890f487e-db98-45dd-a226-c7ccead82b1e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 644e7a9ba26dab15e2bfa2a269f62c04f0510180
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041001"
---
# <a name="linker-tools-warning-lnk4022"></a>링커 도구 경고 LNK4022

'symbol' 기호에만 일치를 찾을 수 없습니다.

주어진된 데코 레이트 되지 않은 기호에 일치 하는 링크 또는 여러 찾을 LIB 및 모호성을 해결 하지 못했습니다. (예:.exe,.dll,.exp, 또는.lib) 출력 파일이 생성 됩니다. 이 경고 뒤에 하나의 경고 [LNK4002](../../error-messages/tool-errors/linker-tools-warning-lnk4002.md) 각각에 대 한 기호를 복제 하 고 마지막으로 심각한 오류 뒤 [LNK1152](../../error-messages/tool-errors/linker-tools-error-lnk1152.md)합니다.

이 경고를 방지 하려면 데코 레이트 된 형태의 기호를 지정 합니다. 실행할 [DUMPBIN](../../build/reference/dumpbin-options.md) 개체에서 참조를 데코 레이트 된 이름입니다.