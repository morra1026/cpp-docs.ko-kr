---
title: 일반적인 MBCS 프로그래밍 팁 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- _mbcs
dev_langs:
- C++
helpviewer_keywords:
- MBCS [C++], dialog box fonts
- MS Shell Dlg
- MBCS [C++], programming
- dialog boxes [C++], fonts
ms.assetid: 7b541235-f3e5-4af0-b2c2-a0112cd5fbfb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: bc27d0b0396fed6e6b03f6c3f8e1f2332fcceecf
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46421104"
---
# <a name="general-mbcs-programming-advice"></a>일반적인 MBCS 프로그래밍 팁

다음 팁을 사용 합니다.

- 유연성을 사용 하 여 런타임에 매크로 같은 `_tcschr` 고 `_tcscpy` 가능한 경우. 자세한 내용은 [Tchar.h의 제네릭 텍스트 매핑](../text/generic-text-mappings-in-tchar-h.md)합니다.

- C 런타임 사용 `_getmbcp` 함수는 현재 코드 페이지 정보를 가져옵니다.

- 문자열 리소스를 다시 사용 하지 마십시오. 대상 언어에 따라 지정 된 문자열로 변환 하는 경우 의미가 될 수 있습니다. 예를 들어 "File" 응용 프로그램의 주 메뉴에서 문자열 "파일" 대화 상자에서 다르게 변환 될 수 있습니다. 동일한 이름을 가진 둘 이상의 문자열을 사용 하는 경우 각각에 대해 다른 문자열 Id를 사용 합니다.

- MBCS 지원 운영 체제에서 응용 프로그램의 실행 여부 확인 하려는 합니다. 이렇게 하려면 프로그램 시작; 플래그를 설정 API 호출에 의존 하지 않습니다.

- 대화 상자를 디자인할 때 허용 약 30 %MBCS 변환에 대 한 정적 텍스트 컨트롤의 끝에 공간을 추가 합니다.

- 일부 글꼴 모든 시스템에서 사용할 수 없기 때문에 응용 프로그램에 대 한 글꼴을 선택할 때 주의 해야 하 고 합니다.

- 사용 하 여 대화 상자에 대 한 글꼴을 선택할 때 [MS Shell Dlg](/windows/desktop/Intl/using-ms-shell-dlg-and-ms-shell-dlg-2) MS Sans Serif 또는 Helvetica 대신 합니다. MS Shell Dlg는 대화 상자를 만들기 전에 시스템에서 올바른 글꼴을 사용 하 여 대체 됩니다. MS Shell Dlg 사용 하면이 글꼴을 사용 하 여 처리 하기 위해 운영 체제의 모든 변경 내용을 자동으로 사용할 수 있도록 합니다. (MFC 대체 MS Shell Dlg는 DEFAULT_GUI_FONT 또는 Windows 95, Windows 98 및 Windows NT 4의 시스템 글꼴을 사용 하 여 해당 시스템 MS Shell Dlg를 올바르게 처리 하지 않습니다.)

- 응용 프로그램을 디자인할 때에 문자열을 지역화할 수를 결정 합니다. 확실 하지 않은의 경우 지정 된 문자열을 지역화 될 예정을 가정 합니다. 따라서 작업만 사용 하 여 지역화할 수 있는 문자열을 혼합 하지 마십시오.

## <a name="see-also"></a>참고 항목

[MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[포인터 증가 및 감소](../text/incrementing-and-decrementing-pointers.md)