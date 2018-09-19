---
title: 링커 도구 경고 LNK4099 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4099
dev_langs:
- C++
helpviewer_keywords:
- LNK4099
ms.assetid: 358170a4-07cd-43fe-918f-82c32757ffc5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 50bdceaba2e72312febec4819b96df334b5398c2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026013"
---
# <a name="linker-tools-warning-lnk4099"></a>링커 도구 경고 LNK4099

' 개체/라이브러리 ' 또는 '경로의'; 'filename' PDB은 찾을 수 없습니다. 디버그 정보가 없는 것 처럼 개체를 링크 합니다.

링커는.pdb 파일을 찾을 수 없습니다. 포함 된 디렉터리에 복사 `object/library`합니다.

개체 파일과 관련 된.pdb 파일의 이름을 찾으려면:

1. 개체 파일을 사용 하 여 라이브러리에서 추출 [lib](../../build/reference/lib-reference.md) **/extract:**`objectname`**.obj** `xyz` **.lib**합니다.

1. 사용 하 여.pdb 파일의 경로를 확인 **/section:.debug$ T /rawdata dumpbin** `objectname` **.obj**합니다.

사용 하 여 컴파일할 수 있습니다 [/z7](../../build/reference/z7-zi-zi-debug-information-format.md)pdb를 사용 하거나 제거할 필요가 없도록, 합니다 [디버그](../../build/reference/debug-generate-debug-info.md) 링커 옵션을 연결 하는 개체에 대 한.pdb 파일이 없는 경우.