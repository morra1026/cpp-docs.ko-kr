---
title: . 링커 입력 파일로 Obj 파일 | Microsoft Docs
ms.custom: ''
ms.date: 12/29/2017
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- linker [C++], OBJ files as input
- object files, linker output
- OMF object files
- LINK tool [C++], .obj files
- COFF files
- OBJ files as linker input
- .obj files as linker input
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ffbc1d7fc7f74121c37c9e80a538ec60f2265701
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43219564"
---
# <a name="obj-files-as-linker-input"></a>링커 입력 파일로 사용하는 .Obj 파일

링커 도구 (링크입니다. EXE).obj 파일에서 개체 파일 형식 COFF (공용)을 허용 합니다.

## <a name="remarks"></a>설명

Microsoft 공용 개체 파일 형식 한 전체 설명을 제공합니다. 자세한 내용은 [PE 형식](/windows/desktop/Debug/pe-format)합니다.

## <a name="unicode-support"></a>유니코드 지원

Visual Studio 2005 부터는 Microsoft Visual c + + 컴파일러는 ISO/IEC C 및 c + + 표준에 정의 된 대로 식별자의 유니코드 문자를 지원 합니다. 이전 버전의 컴파일러는 식별자에 ASCII 문자만 지원 합니다. 함수, 클래스 및 정적 변수 이름에 유니코드를 지원 하기 위해 컴파일러 및 링커에서의 유니코드 u t F-8 인코딩을 사용.obj 파일에 COFF 기호에 대 한 합니다. 인코딩을 u t F-8 이전 버전의 Visual Studio에서 사용 하는 ASCII 인코딩을 사용 하 여 만들어졌기 호환있지 않습니다.

컴파일러 및 링커에 대 한 자세한 내용은 참조 하세요. [컴파일러 및 링커에서의 유니코드 지원](../../build/reference/unicode-support-in-the-compiler-and-linker.md)합니다. 유니코드 표준에 대 한 자세한 내용은 참조는 [유니코드](http://go.microsoft.com/fwlink/p/?linkid=37123) 조직입니다.

## <a name="see-also"></a>참고자료

[LINK 입력 파일](../../build/reference/link-input-files.md)  
[링커 옵션](../../build/reference/linker-options.md)  
[유니코드 지원](../../text/support-for-unicode.md)  
[컴파일러 및 링커에서의 유니코드 지원](../../build/reference/unicode-support-in-the-compiler-and-linker.md)  
[유니코드 표준](http://go.microsoft.com/fwlink/p/?linkid=37123)  
[PE 형식](/windows/desktop/Debug/pe-format)  
