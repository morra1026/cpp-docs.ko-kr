---
title: 'Catlservicemodulet:: Start 함수'
ms.date: 11/04/2016
f1_keywords:
- CServiceModule.Start
- CServiceModule::Start
helpviewer_keywords:
- Start method
ms.assetid: b5193a23-41bc-42d2-8d55-3eb43dc62238
ms.openlocfilehash: 806cd8ec353e2111d249472fb9aa885e7548baab
ms.sourcegitcommit: c3093251193944840e3d0a068ecc30e6449624ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57265160"
---
# <a name="catlservicemoduletstart-function"></a>Catlservicemodulet:: Start 함수

서비스가 실행 되 면 `_tWinMain` 호출 `CAtlServiceModuleT::WinMain`를 호출 하 `CAtlServiceModuleT::Start`합니다.

`CAtlServiceModuleT::Start` 배열을 설정 `SERVICE_TABLE_ENTRY` 각 서비스는 시작 함수에 매핑되는 구조입니다. 이 배열은 Win32 API 함수에 전달 됩니다 [StartServiceCtrlDispatcher](/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera)합니다. 이론적으로 하나의 EXE 여러 서비스를 처리할 수 및 배열에는 여러 개 있을 수 있습니다 `SERVICE_TABLE_ENTRY` 구조입니다. 그러나 현재 ATL에서 생성 된 서비스를 지 원하는 EXE 당 하나의 서비스입니다. 따라서 배열에 서비스 이름을 포함 하는 단일 항목 및 `_ServiceMain` 함수로 시작 합니다. `_ServiceMain` 정적 멤버 함수인 `CAtlServiceModuleT` 비정적 멤버 함수를 호출 하는 `ServiceMain`합니다.

> [!NOTE]
>  오류의 `StartServiceCtrlDispatcher` 서비스 컨트롤에 연결할 관리자 (SCM) 의미할 프로그램을 서비스로 실행 하지. 이 경우 프로그램 호출 `CAtlServiceModuleT::Run` 직접 로컬 서버로 프로그램을 실행할 수 있도록 합니다. 로컬 서버로 프로그램을 실행 하는 방법에 대 한 자세한 내용은 참조 하세요. [디버깅 팁](../atl/debugging-tips.md)합니다.

## <a name="see-also"></a>참고자료

[서비스](../atl/atl-services.md)<br/>
[CAtlServiceModuleT::Start](../atl/reference/catlservicemodulet-class.md#start)
