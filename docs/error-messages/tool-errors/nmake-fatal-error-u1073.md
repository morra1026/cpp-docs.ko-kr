---
title: NMAKE 심각한 오류 U1073 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1073
dev_langs:
- C++
helpviewer_keywords:
- U1073
ms.assetid: d46bf2dd-400a-4802-9db2-f832e1c97f02
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4c309ed94cd1c984406e0d21f0139e35c6e41d7d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46053944"
---
# <a name="nmake-fatal-error-u1073"></a>NMAKE 심각한 오류 U1073

'targetname'를 확인 하는 방법을 몰라도합니다

지정된 된 대상 없고 실행할 명령 또는 유추 규칙을 적용 하지 않습니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 대상 이름의 철자를 확인 합니다.

1. 하는 경우 *targetname* 는 의사는 다른 설명 블록에 대상으로 지정 합니다.

1. 하는 경우 *targetname* 는 매크로 호출을 null 문자열로 확장 되지 않고 해야 합니다.