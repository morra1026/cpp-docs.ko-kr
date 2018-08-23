---
title: -ALLOWBIND (DLL 바인딩 방지) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.PreventDLLBinding
- /allowbind
dev_langs:
- C++
helpviewer_keywords:
- /ALLOWBIND linker option
- binding DLLs
- preventing DLL binding
- ALLOWBIND linker option
- -ALLOWBIND linker option
- DLLs [C++], preventing binding
ms.assetid: 30e37e24-12e4-407e-988a-39d357403598
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a0bff9ec6502aab5787c492a15e008bc29926163
ms.sourcegitcommit: b92ca0b74f0b00372709e81333885750ba91f90e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/16/2018
ms.locfileid: "42572312"
---
# <a name="allowbind-prevent-dll-binding"></a>/ALLOWBIND(DLL 바인딩 방지)
```  
/ALLOWBIND[:NO]  
```  
  
## <a name="remarks"></a>설명  
 /ALLOWBIND:NO는 DLL의 헤더에서 이미지 바인딩을 허용하지 않는 Bind.exe를 가리키는 비트를 설정합니다. 바인딩이 서명을 무효화하므로 디지털 서명된 경우 DLL을 바인딩하지 않으려고 할 수 있습니다.  
  
 사용 하 여 여 /ALLOWBIND 기능의 기존 DLL을 편집할 수는 [여 /ALLOWBIND](../../build/reference/allowbind.md) EDITBIN 유틸리티의 옵션입니다.  
  
### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면  
  
1.  프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.  
  
2.  확장 **구성 속성**를 **링커**를 선택 하 고 **명령줄**합니다.  
  
3.  입력 `/ALLOWBIND:NO` 로 **추가 옵션**합니다.  
  
### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면  
  
-   <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [링커 옵션 설정](../../build/reference/setting-linker-options.md)   
 [링커 옵션](../../build/reference/linker-options.md)   
 [BindImage 함수](/windows/desktop/api/imagehlp/nf-imagehlp-bindimage)   
 [BindImageEx 함수](/windows/desktop/api/imagehlp/nf-imagehlp-bindimageex)