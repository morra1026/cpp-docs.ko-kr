---
title: . 링커 입력 파일로 lib 파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.AdditionalDependencies
dev_langs:
- C++
helpviewer_keywords:
- OMF libraries
- linking [C++], OMF libraries
- import libraries, linker files
- libraries [C++], .lib files as linker input
- COFF files, import libraries
- default libraries [C++], linker output
- default libraries [C++]
- defaults [C++], libraries
- .lib files
ms.assetid: dc5d2b1c-2487-41fa-aa71-ad1e0647958b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 774fe236b66bbe6222956de05efbfe89fab3de9f
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45706500"
---
# <a name="lib-files-as-linker-input"></a>링커 입력 파일로 사용하는 .Lib 파일

링크 허용 COFF 표준 라이브러리 및 COFF 가져오기 라이브러리를 모두 일반적으로 확장명이. lib 합니다. 표준 라이브러리 개체를 포함 하 고 라이브러리 도구에서 생성 됩니다. 가져오기 라이브러리 다른 프로그램의 내보내기에 대 한 정보를 포함 및 내보내기가 포함 된 프로그램을 빌드할 때 링크로 하거나 LIB 도구에서 만듭니다. LIB 표준 만들기 또는 가져오기 라이브러리를 사용에 대 한 내용은 참조 하세요 [LIB 참조](../../build/reference/lib-reference.md)합니다. 링크를 사용 하 여 가져오기 라이브러리를 만드는 데 대 한 내용은 참조는 [/DLL](../../build/reference/dll-build-a-dll.md) 옵션입니다.

라이브러리는 파일 이름 인수 또는 기본 라이브러리 링크로 지정 됩니다. 링크 명령줄에 지정 된 라이브러리에서 먼저 검색 하 여 외부 참조를 확인 하 여 라이브러리 지정 하는 기본 합니다 [/DEFAULTLIB](../../build/reference/defaultlib-specify-default-library.md) 옵션을 다음 기본 라이브러리 파일에 지정 된.obj 및 합니다. 라이브러리 이름 없이 경로 지정한 경우 링크 디렉터리에 있는 라이브러리를 찾습니다. 경로가 지정 되지 않은, 경우 LINK에서는 먼저 링크를 실행 하는 디렉터리에서 찾은 다음 LIB 환경 변수에 지정 된 디렉터리에서 찾습니다.

## <a name="to-add-lib-files-as-linker-input-in-the-development-environment"></a>개발 환경에서 링커 입력 파일로.lib 파일을 추가 하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **입력** 속성 페이지에는 **링커** 폴더.

1. 수정 된 **추가 종속성** .lib 파일에 추가할 속성입니다.

## <a name="to-programmatically-add-lib-files-as-linker-input"></a>프로그래밍 방식으로 링커 입력 파일로.lib 파일을 추가 하려면

- 참조 [AdditionalDependencies](https://msdn.microsoft.com/library/microsoft.visualstudio.vcprojectengine.vclinkertool.additionaldependencies.aspx)합니다.

## <a name="example"></a>예제

다음 샘플을 빌드하고.lib 파일을 사용 하는 방법을 보여 줍니다. 첫째,.lib 파일을 빌드하십시오.

```cpp
// lib_link_input_1.cpp
// compile by using: cl /LD lib_link_input_1.cpp
__declspec(dllexport) int Test() {
   return 213;
}
```

고 그런 다음 방금 만든.lib 파일을 사용 하 여이 샘플을 컴파일 하세요.

```cpp
// lib_link_input_2.cpp
// compile by using: cl /EHsc lib_link_input_1.lib lib_link_input_2.cpp
__declspec(dllimport) int Test();
#include <iostream>
int main() {
   std::cout << Test() << std::endl;
}
```

```Output
213
```

## <a name="see-also"></a>참고 항목

[LINK 입력 파일](../../build/reference/link-input-files.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)