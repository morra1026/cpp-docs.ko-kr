---
title: 링커 도구 오류 LNK1140 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1140
dev_langs:
- C++
helpviewer_keywords:
- LNK1140
ms.assetid: 468d7651-a7cd-47b9-aead-5bb2fab56121
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9f850360bc749a41e548cebae9f58f9fc7d3d420
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46044706"
---
# <a name="linker-tools-error-lnk1140"></a>링커 도구 오류 LNK1140

프로그램 데이터베이스에 대 한 너무 많은 모듈 링크 /PDB: NONE

프로젝트에 4,096 개가 넘는 모듈이 있습니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 사용 하 여 다시 연결 [/PDB: NONE](../../build/reference/pdb-use-program-database.md)합니다.

1. 정보를 디버깅 하지 않고 일부 모듈을 컴파일하십시오.

1. 모듈의 수를 줄입니다.