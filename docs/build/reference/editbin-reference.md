---
title: EDITBIN 참조 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- editbin
dev_langs:
- C++
helpviewer_keywords:
- binary data, editing
- object files, modifying
- EDITBIN program
- COFF files, editing
ms.assetid: efdda03b-3dfc-4d31-90e6-caf5b3977914
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 809d1d4f25611b2310d651702f01e1e98888ad4a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45699949"
---
# <a name="editbin-reference"></a>EDITBIN 참조

Microsoft COFF Binary 파일 편집기 (EDITBIN 합니다. EXE) 개체 파일 형식 COFF (공용) 이진 파일을 수정 합니다. 개체 파일, 실행 파일 및 동적 연결 라이브러리 (DLL)를 수정 하려면 EDITBIN를 사용할 수 있습니다.

> [!NOTE]
>  Visual Studio 명령 프롬프트 에서만에서이 도구를 시작할 수 있습니다. 시스템 명령 프롬프트 또는 파일 탐색기에서는 시작할 수 없습니다.

EDITBIN를 사용 하 여 생성 된 파일에서 사용 하기 위해 사용할 수 없는 합니다 [/GL](../../build/reference/gl-whole-program-optimization.md) 컴파일러 옵션입니다. 다시 컴파일 및 연결 하 여 구현할 수 /GL을 사용 하 여 생성 된 이진 파일을 수정 해야 합니다.

- [EDITBIN 명령줄](../../build/reference/editbin-command-line.md)

- [EDITBIN 옵션](../../build/reference/editbin-options.md)

## <a name="see-also"></a>참고 항목

[ 빌드 도구](../../build/reference/c-cpp-build-tools.md)