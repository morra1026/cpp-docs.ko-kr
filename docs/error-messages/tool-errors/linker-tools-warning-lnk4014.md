---
title: 링커 도구 경고 LNK4014 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4014
dev_langs:
- C++
helpviewer_keywords:
- LNK4014
ms.assetid: 394903e9-3ded-4ea4-b7c0-a3535d4b4da4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: df0a3b6f30733413a0f27c0b8daa07394bb04b07
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46023113"
---
# <a name="linker-tools-warning-lnk4014"></a>링커 도구 경고 LNK4014

멤버 개체 "objectname"를 찾을 수 없습니다.

LIB 찾지 `objectname` 라이브러리에서.

**/제거** 하 고 **추출/** 옵션 삭제 하거나 파일에 복사 하는 멤버 개체의 전체 이름에 필요 합니다. 원래 개체 파일의 경로 포함 하는 전체 이름입니다. 라이브러리에 있는 멤버 개체의 전체 이름을 보려면 사용 DUMPBIN [/ARCHIVEMEMBERS](../../build/reference/archivemembers.md) 또는 LIB [/list](../../build/reference/managing-a-library.md)합니다.