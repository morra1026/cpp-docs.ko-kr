---
title: 다중 인라인 파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- inline files, multiple NMAKE
- multiple inline files
- NMAKE program, inline files
ms.assetid: 6d381dcf-0ed8-45d1-8df3-b4598d860b99
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 87d68034c4f0018d65020915d24d0b5c2ec5d61a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725597"
---
# <a name="multiple-inline-files"></a>인라인 파일이 여러 개인 경우

명령을은 인라인 파일이 여러 개 만들 수 있습니다.

## <a name="syntax"></a>구문

```
command << <<
inlinetext
<<[KEEP | NOKEEP]
inlinetext
<<[KEEP | NOKEEP]
```

## <a name="remarks"></a>설명

각 파일에 대해 하나 이상의 줄 뒤에 닫는 줄 구분 기호를 포함 하는 인라인 텍스트를 지정 합니다. 첫 번째 파일의 구분 줄을 다음 줄에 두 번째 파일의 텍스트를 시작 합니다.

## <a name="see-also"></a>참고 항목

[메이크파일의 인라인 파일](../build/inline-files-in-a-makefile.md)