---
title: 링커 도구 오류 LNK1201 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1201
dev_langs:
- C++
helpviewer_keywords:
- LNK1201
ms.assetid: 64c3f496-a428-4b54-981e-faa82ef9c8a1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4c133748f95846160e1387e31e023d9ce459b281
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055274"
---
# <a name="linker-tools-error-lnk1201"></a>링커 도구 오류 LNK1201

'filename'; 프로그램 데이터베이스에 쓰는 동안 오류 발생 디스크 공간 부족, 잘못 된 경로 또는 권한이 부족 하 여 확인

연결은 프로그램 데이터베이스 (PDB) 출력 파일에 쓸 수 없습니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 파일이 손상 되었습니다. PDB 파일 및 다시 연결을 삭제 합니다.

1. 파일을 쓸 디스크 공간이 부족 합니다.

1. 드라이브를 네트워크 문제로 인해 사용할 수 없습니다.

1. 디버거 연결 하려는 프로그램 활성화 됩니다.

1. 힙 공간이 부족 합니다.  참조 [C1060](../../error-messages/compiler-errors-1/fatal-error-c1060.md) 자세한 내용은 합니다.