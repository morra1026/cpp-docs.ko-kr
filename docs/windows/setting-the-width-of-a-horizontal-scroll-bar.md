---
title: 가로 스크롤 막대 너비 설정
ms.date: 11/04/2016
helpviewer_keywords:
- list controls [C++], scroll bar width
- CListBox::SetHorizontalExtent
- controls [C++], scroll bar
- scroll bars [C++], displaying in controls
- horizontal scroll bar width
- CListBox class, scroll bar width
- scroll bars [C++], width
ms.assetid: 51dad141-aa0b-46a3-a82c-46b80d603d94
ms.openlocfilehash: 393571b79d27485e840d150549208c899e8ed1d2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50625955"
---
# <a name="setting-the-width-of-a-horizontal-scroll-bar"></a>가로 스크롤 막대 너비 설정

MFC 클래스를 사용 하 여 대화 상자에 가로 스크롤 막대를 사용 하 여 목록 상자를 추가 하면 응용 프로그램에서 스크롤 막대를 자동으로 나타나지 않습니다.

### <a name="to-make-the-scroll-bar-appear"></a>스크롤 막대 표시를 확인 합니다.

1. 호출 하 여 광범위 한 요소에 대 한 최대 너비를 설정할 [CListBox::SetHorizontalExtent](../mfc/reference/clistbox-class.md#sethorizontalextent) 코드에서.

   이 값을 설정 하지 않고 스크롤 막대 표시 되지 않습니다에 목록 상자의 항목 상자 보다 넓을 경우.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리 되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대 한 내용은 참조 하세요 [데스크톱 앱에 대 한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)합니다. 전역화 및 지역화 관리 되는 앱의 리소스에 대 한 내용은 참조 하세요 [Globalizing and Localizing.NET Framework Applications](/dotnet/standard/globalization-localization/index)합니다.

## <a name="requirements"></a>요구 사항

MFC

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)