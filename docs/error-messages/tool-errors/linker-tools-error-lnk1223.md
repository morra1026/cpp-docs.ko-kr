---
title: 링커 도구 오류 LNK1223 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1223
dev_langs:
- C++
helpviewer_keywords:
- LNK1223
ms.assetid: c4728c36-daee-462f-a1c7-8733dcdec88e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8639919c74559829367108b36d62594e2a83a91a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067993"
---
# <a name="linker-tools-error-lnk1223"></a>링커 도구 오류 LNK1223

파일이 잘못되었거나 손상되었습니다. 파일의 .pdata 정보가 잘못되었습니다.

pdata를 사용하는 RISC 플랫폼에서는 컴파일러가 정렬되지 않은 항목을 포함하는 .pdata 섹션을 내보낼 때 이 오류가 발생합니다.

이 문제를 해결 하려면 없이 컴파일을 시도 [/GL (전체 프로그램 최적화)](../../error-messages/tool-errors/linker-tools-error-lnk1223.md) 사용 하도록 설정 합니다. 빈 함수 본문으로 인해 이 오류가 발생하는 경우도 있습니다.