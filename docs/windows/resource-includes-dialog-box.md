---
title: 리소스 내용 대화 상자 (c + +)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.resourceincludes
helpviewer_keywords:
- Resource Includes dialog box [C++]
- rc files [C++], changing storage
- symbol header files [C++], changing
- .rc files [C++], changing storage
- symbol header files [C++], read-only
- symbols [C++], symbol header files
ms.assetid: 659a54e6-e416-4045-8411-798730ff4ce3
ms.openlocfilehash: b0e7125e07deb965055da54126eb0933e64c0429
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50625061"
---
# <a name="resource-includes-dialog-box-c"></a>리소스 내용 대화 상자 (c + +)

사용할 수는 **리소스 내용** 환경의 기본 작업 수정할에서 프로젝트.rc 파일 및 모든 리소스를 모두 저장 하는 c + + 프로젝트의 대화 상자 [기호](../windows/symbols-resource-identifiers.md) Resource.h에 있습니다.

열려는 합니다 **리소스 내용** 대화 상자에서 마우스 오른쪽 단추로 클릭.rc 파일 [리소스 뷰](../windows/resource-view-window.md), 선택한 **리소스 내용** 바로 가기 메뉴에서.

- **기호 헤더 파일**

   리소스 파일에 대한 기호 정의가 저장되는 헤더 파일의 이름을 변경할 수 있습니다. 자세한 내용은 [기호 헤더 파일의 이름 변경](../windows/changing-the-names-of-symbol-header-files.md)합니다.

- **읽기 전용 기호 지시문**

   편집 세션 동안 수정해서는 안 되는 기호가 들어 있는 헤더 파일을 포함할 수 있습니다. 예를 들어 여러 프로젝트 간에 공유되는 기호 파일을 포함할 수 있습니다. MFC .h 파일을 포함할 수도 있습니다. 자세한 내용은 [비롯 한 공유 (읽기 전용) 또는 계산 된 기호](../windows/including-shared-read-only-or-calculated-symbols.md)합니다.

- **컴파일 시간 지시문**

   기본 리소스 파일에 있는 리소스와 별도로 생성 및 편집되는 리소스 파일을 포함하거나, 컴파일 시간 지시문(예: 특정 조건에 따라 리소스를 포함하는 지시문)을 포함하거나, 사용자 지정 형식에 리소스를 포함할 수 있습니다. 사용할 수도 있습니다는 **컴파일 시간 지시문 상자** 표준 MFC 리소스 파일을 포함 합니다. 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다.

> [!NOTE]
> 이러한 텍스트 상자에 항목으로 표시.rc 파일에 나타나는 `TEXTINCLUDE 1`, `TEXTINCLUDE 2`, 및 `TEXTINCLUDE 3` 각각. 자세한 내용은 [TN035:를 사용 하 여 여러 리소스 파일과 헤더 파일 Visual c + +를 사용 하 여](../mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp.md)입니다.

사용 하 여 리소스 파일에 변경 내용을 적용 하 고 나면 합니다 **리소스 내용** .rc 파일을 닫은 다음 다시 변경 내용을 적용 하려면 필요한 대화 상자. 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[방법: 리소스 포함 디렉터리 지정](../windows/how-to-specify-include-directories-for-resources.md)<br/>
[기호: 리소스 식별자](../windows/symbols-resource-identifiers.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)