---
title: 리소스 (c + +)에 대 한 편집 가능한 파일 형식
ms.date: 11/04/2016
f1_keywords:
- vc.editors.resource
helpviewer_keywords:
- file types [C++], for resources
- resources [C++], editing
- files [C++], editable types
- resource editing
ms.assetid: c40f9204-f2f2-400b-9f53-53b7bf291356
ms.openlocfilehash: 9f688c144a3453c2de849b36f34f6a465e3dfeae
ms.sourcegitcommit: 5a7dbd640376e13379f5d5b2cf66c4842e5e737b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55905721"
---
# <a name="editable-file-types-for-resources-c"></a>리소스 (c + +)에 대 한 편집 가능한 파일 형식

다음 형식의 파일을 열고 포함된 리소스를 편집할 수 있습니다.

|파일 이름|설명|
|---------------|-----------------|
|.rc|리소스 스크립트 파일입니다.|
|.rct|리소스 템플릿 파일입니다.|
|.res|리소스 파일입니다.|
|.resx|관리되는 리소스 파일입니다.|
|.exe|실행 파일입니다.|
|.dll|동적 연결 라이브러리 파일입니다.|
|.bmp, .ico, .dib, and .cur|비트맵, 아이콘, 도구 모음 및 커서 파일입니다.|

## <a name="files-affected-by-resource-editing"></a>리소스 편집의 영향을 받는 파일

Visual Studio 환경은 리소스 편집 세션 중 다음 표에 표시된 파일에서 작동합니다.

|파일 이름|설명|
|---------------|-----------------|
|Resource.h|개발 환경에서 생성된 헤더 파일로, 기호 정의를 포함합니다. (소스 제어에이 파일을 포함 합니다.)|
|Filename.aps|현재 리소스 스크립트 파일의 이진 버전으로, 빠른 로드를 위해 사용됩니다.<br /><br /> 리소스 편집기에서 .rc 또는 resource.h 파일을 직접 읽지 않습니다. 리소스 컴파일러는 리소스 편집기에서 사용되는 이러한 파일을 .aps 파일로 컴파일합니다. 이 파일은 컴파일 단계이며 기호화된 데이터만 저장합니다. 일반적인 컴파일 프로세스에서처럼 기호화되지 않은 정보(예: 주석)는 컴파일 프로세스 중에 삭제됩니다. .aps 파일이 .rc 파일과 동기화되지 않을 때마다 .rc 파일이 다시 생성됩니다. 예를 들어 저장하면 리소스 편집기에서 .rc 파일 및 resource.h 파일을 덮어씁니다. 리소스 자체의 모든 변경 내용은 .rc 파일에 통합된 상태로 유지되지만 주석은 .rc 파일을 덮어쓰면 항상 손실됩니다. 주석을 유지 하는 방법에 대 한 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다. (일반적으로 있습니다 포함 되지 않습니다.aps 파일이 소스 제어에.)|
|.rc|현재 프로젝트의 리소스에 대한 스크립트가 포함된 리소스 스크립트 파일입니다. 저장할 때마다 .aps 파일이 이 파일을 덮어씁니다. (소스 제어에이 파일을 포함 합니다.)|

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일](../windows/resource-files-visual-studio.md)