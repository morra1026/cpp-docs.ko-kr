---
title: MFC DLL 마법사, 응용 프로그램 설정 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- vc.appwiz.mfc.dll.appset
dev_langs:
- C++
helpviewer_keywords:
- MFC DLL Wizard, application settings
ms.assetid: 0a96b94f-ae36-4975-951b-c9ffb3def21c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a96b166f5fc2873736d01438d91fc971120abf2e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46437042"
---
# <a name="application-settings-mfc-dll-wizard"></a>MFC DLL 마법사, 응용 프로그램 설정

MFC DLL 마법사의이 페이지를 사용 하 여 디자인 하 고 새 MFC DLL 프로젝트에 기본 기능을 추가 합니다.

## <a name="dll-type"></a>DLL 형식

생성 하려는 DLL의 유형을 선택 합니다.

- **공유 MFC DLL을 사용 하 여 기본 MFC DLL**

   MFC 라이브러리를 공유 DLL로 프로그램에 연결 하려면이 옵션을 선택 합니다. 이 옵션을 사용 하면 DLL 및 호출 응용 프로그램 간의 MFC 개체를 공유할 수 없습니다. 프로그램에서는 런타임에 MFC 라이브러리를 호출 합니다. 이 옵션 MFC 라이브러리를 사용 하는 여러 실행 파일의 구성 된 경우 프로그램의 디스크 및 메모리 요구 사항이 줄어듭니다. Win32와 MFC 프로그램 DLL의 함수를 호출할 수 있습니다. 이 유형의 프로젝트를 사용 하 여 MFC DLL을 재배포 해야 합니다.

- **MFC 사용 하 여 기본 MFC DLL을 정적으로 링크**

   빌드 시간에 정적으로 MFC 라이브러리에 프로그램을 연결 하려면이 옵션을 선택 합니다. Win32와 MFC 프로그램 DLL의 함수를 호출할 수 있습니다. 이 옵션에는 프로그램의 크기 증가 하면이 유형의 프로젝트를 사용 하 여 MFC DLL을 다시 배포할 필요가 없습니다. MFC 개체 DLL 및 호출 응용 프로그램 간에 공유할 수 없습니다.

- **MFC 확장명 DLL**

   프로그램 실행 시, MFC 라이브러리를 호출 하 고 호출 응용 프로그램 및 DLL 간에 MFC 개체를 공유 하려는 경우이 옵션을 선택 합니다. 이 옵션 모두 MFC 라이브러리를 사용 하는 여러 실행 파일의 구성 된 경우 프로그램의 디스크 및 메모리 요구 사항이 줄어듭니다. MFC 프로그램에만 DLL의 함수를 호출할 수 있습니다. 이 유형의 프로젝트를 사용 하 여 MFC DLL을 재배포 해야 합니다.

## <a name="additional-features"></a>추가 기능

MFC DLL 자동화를 지원 해야 하는지 여부를 및 Windows 소켓을 지원 해야 하는지 여부를 선택 합니다.

- **자동화**

   선택 **Automation** 를 프로그램에서 다른 프로그램에서 구현 된 개체를 조작할 수 있도록 합니다. 선택 **Automation** 도 다른 자동화 클라이언트에 프로그램을 노출 합니다. 참조 [Automation](../../mfc/automation.md) 자세한 내용은 합니다.

- **Windows 소켓**

   Windows 소켓 프로그램 지원함을 나타내려면이 옵션을 선택 합니다. Windows 소켓을 사용 하면 TCP/IP 네트워크를 통해 통신 하는 프로그램을 작성할 수 있습니다.

   Windows 사용 하 여 MFC DLL 소켓 지원 만들어집니다 [CWinApp::InitInstance](../../mfc/reference/cwinapp-class.md#initinstance) 초기화 소켓에 대 한 지원 및 MFC 헤더 파일 StdAfx.h AfxSock.h 포함 되어 있습니다.

## <a name="see-also"></a>참고 항목

[MFC DLL 마법사](../../mfc/reference/mfc-dll-wizard.md)<br/>
[MFC DLL 프로젝트 만들기](../../mfc/reference/creating-an-mfc-dll-project.md)

