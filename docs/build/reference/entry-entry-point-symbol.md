---
title: -ENTRY (진입점 기호) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /entry
- VC.Project.VCLinkerTool.EntryPointSymbol
dev_langs:
- C++
helpviewer_keywords:
- starting address
- -ENTRY linker option
- /ENTRY linker option
- ENTRY linker option
ms.assetid: 26c62ba2-4f52-4882-a7bd-7046a0abf445
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 53f5a18b061cbd956731ced6788e86f871ea97bd
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45719578"
---
# <a name="entry-entry-point-symbol"></a>/ENTRY(진입점 기호)

```
/ENTRY:function
```

## <a name="arguments"></a>인수

*function*<br/>
사용자 정의 시작을 지정 하는 함수를.exe 파일이 나 DLL에 대 한 주소입니다.

## <a name="remarks"></a>설명

/ENTRY 옵션은.exe 파일 또는 DLL의 시작 주소로 진입점 함수를 지정합니다.

사용 하도록 함수를 정의 해야 합니다 `__stdcall` 호출 규칙입니다. 매개 변수 및 반환 값에 따라 달라 집니다 프로그램이 콘솔 응용 프로그램, windows 응용 프로그램 또는 DLL입니다. C 런타임 라이브러리를 올바르게 초기화 되 고 정적 개체에 대 한 c + + 생성자가 실행 되도록 진입점을 설정 하는 링커를 사용 하는 것이 좋습니다.

기본적으로 시작 주소에는 C 런타임 라이브러리에서 함수 이름입니다. 링커는 다음 표에 나와 있는 것 처럼 해당 프로그램의 특성에 따라 선택 합니다.

|함수 이름|에 대 한 기본값|
|-------------------|-----------------|
|**mainCRTStartup** (또는 **wmainCRTStartup**)|/Subsystem: console;를 사용 하는 응용 프로그램 호출 `main` (또는 `wmain`)|
|**WinMainCRTStartup** (또는 **wWinMainCRTStartup**)|/SUBSYSTEM을 사용 하는 응용 프로그램:**WINDOWS**; 호출 `WinMain` (또는 `wWinMain`)를 사용 하 여 정의 되어야 합니다는 `__stdcall`|
|**_DllMainCRTStartup**|DLL; 호출 `DllMain` 존재 하는 경우는 정의 되어야 합니다 사용 `__stdcall`|

경우는 [/DLL](../../build/reference/dll-build-a-dll.md) 또는 [/SUBSYSTEM](../../build/reference/subsystem-specify-subsystem.md) 옵션을 지정 하지, 링커 선택 여부에 따라 하위 시스템 및 항목 지점 `main` 또는 `WinMain` 정의 됩니다.

함수 `main`, `WinMain`, 및 `DllMain` 사용자 정의 진입점에 세 가지입니다.

/ENTRY를 지정 하는 함수의 서명이 있어야 관리 되는 이미지를 만들 때 (LPVOID *var1*, DWORD *var2*, LPVOID *var3*).

사용자 지정 하는 방법에 대 한 내용은 `DllMain` 진입점 참조 [Dll 및 Visual c + + 런타임 라이브러리 동작](../../build/run-time-library-behavior.md) 합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **고급** 속성 페이지.

1. 수정 된 **진입점** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.EntryPointSymbol%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)