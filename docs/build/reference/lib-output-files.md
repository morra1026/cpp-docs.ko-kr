---
title: LIB 출력 파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- Lib
dev_langs:
- C++
helpviewer_keywords:
- output files, LIB
ms.assetid: e73d2f9b-a42d-402b-b7e3-3a94bebb317e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 23665897266bab87c71b8b3889688113fe8aa99a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45720709"
---
# <a name="lib-output-files"></a>LIB 출력 파일

LIB에서 생성 된 출력 파일 표에 표시 된 것 처럼가 사용 되 고 있는 모드에 따라 달라 집니다.

|모드|출력|
|----------|------------|
|기본값 (빌드 또는 라이브러리를 수정 합니다.)|COFF 라이브러리 (.lib)|
|/EXTRACT을 사용 하 여 멤버 추출|개체 (.obj) 파일|
|내보내기 파일을 빌드하고 /def 라이브러리 가져오기|라이브러리 (.lib) 및 내보내기 (.exp) 파일 가져오기|

## <a name="see-also"></a>참고 항목

[LIB 개요](../../build/reference/overview-of-lib.md)