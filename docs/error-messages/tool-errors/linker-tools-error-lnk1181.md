---
title: 링커 도구 오류 LNK1181 | Microsoft Docs
ms.custom: ''
ms.date: 08/22/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1181
dev_langs:
- C++
helpviewer_keywords:
- LNK1181
ms.assetid: 984b0db6-e331-4284-b2a7-a212fe96c486
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 787c6c35b698b5dce57c4aaf3acb4eca496ead95
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50072163"
---
# <a name="linker-tools-error-lnk1181"></a>링커 도구 오류 LNK1181

'filename' 입력된 파일을 열 수 없습니다.

링커를 찾지 `filename` 없거나 경로 때문입니다.

오류 LNK1181 포함에 대 한 몇 가지 일반적 원인:

- `filename` 링커 줄 하지만 파일에 추가 종속성이 존재 하지 않으므로 참조 됩니다.

- A **/LIBPATH** 포함 하는 디렉터리를 지정 하는 문을 `filename` 누락 되었습니다.

위의 문제를 해결 하려면 링커 줄에서 참조 되는 모든 파일 시스템에 있는지를 확인 합니다.  또한 한지를 확인 합니다.는 **/LIBPATH** 링커 종속 파일이 포함 된 각 디렉터리에 대 한 문입니다.

자세한 내용은 [링커 입력 파일로.lib 파일](../../build/reference/dot-lib-files-as-linker-input.md)합니다.

다른 가능한 원인은 LNK1181 공백이 포함된 된 긴 파일 이름을 따옴표로 묶지 된 경우  링커는만 첫 번째 공백 까지의 파일 이름으로 인식 하 고 파일 확장명으로 간주 하는 경우. obj.  이 상황을 해결 방법은 긴 파일 이름을 묶습니다 (경로 파일 이름) 따옴표로 합니다.

사용 하 여 컴파일하는 [/P (파일로 전처리)](../../build/reference/p-preprocess-to-a-file.md) 옵션 LNK1181 해당 옵션.obj 파일의 생성을 억제 하기 때문에 발생할 수 있습니다.

## <a name="see-also"></a>참고 항목

[/LIBPATH(추가 Libpath)](../../build/reference/libpath-additional-libpath.md)