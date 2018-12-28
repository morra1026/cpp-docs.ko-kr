---
title: 일반적인 MBCS 프로그래밍 팁
ms.date: 11/04/2016
f1_keywords:
- _mbcs
helpviewer_keywords:
- MBCS [C++], dialog box fonts
- MS Shell Dlg
- MBCS [C++], programming
- dialog boxes [C++], fonts
ms.assetid: 7b541235-f3e5-4af0-b2c2-a0112cd5fbfb
ms.openlocfilehash: 800e94bfb8a52b806ad45368499f126fbf163389
ms.sourcegitcommit: ff3cbe4235b6c316edcc7677f79f70c3e784ad76
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53626697"
---
# <a name="general-mbcs-programming-advice"></a>일반적인 MBCS 프로그래밍 팁

다음의 MBCS 프로그래밍 팁을 참고하세요.

- 코드의 유연성을 위해 가급적 `_tcschr`나 `_tcscpy`와 같은 런타임 매크로를 사용하세요. 자세한 내용은 [tchar.h의 제네릭 텍스트 매핑](../text/generic-text-mappings-in-tchar-h.md)합니다.

- C 런타임의 `_getmbcp` 함수는 현재 코드 페이지 정보를 가져옵니다.

- 공간 낭비를 줄이기 위한 목적으로 문자열 리소스에 포함된 다른 곳에서 사용하는 문자열을 다시 사용하지 마십시오. 대상 언어에 따라 번역 과정을 거치면서 재사용한 문자열이 다른 의미를 가질 수 있습니다. 예를 들어 응용 프로그램 주 메뉴의 File'이 번역된 '파일'은 대화상자의 'File' 문자열과 다르게 번역될 수 있습니다. 동일한 이름을 가진 둘 이상의 문자열을 사용하는 경우 각 문자열마다 다른 문자열 ID를 사용합니다.

- MBCS 지원 운영 체제에서 응용 프로그램의 실행 여부 확인 하려는 합니다. 이렇게 하려면 프로그램 시작; 플래그를 설정 API 호출에 의존 하지 않습니다.

- 대화 상자를 디자인할 때 멀티바이트 문자 집합(MBCS) 변환을 위해 정적 텍스트 컨트롤 끝 부분에 약 30% 정도의 추가 공간을 확보하세요.

- 일부 글꼴은 모든 시스템에서 사용하지 못할 수도 있으므로, 애플리케이션에서 글꼴을 사용할 때 주의해야 합니다.

- 사용 하 여 대화 상자에 대 한 글꼴을 선택할 때 [MS Shell Dlg](/windows/desktop/Intl/using-ms-shell-dlg-and-ms-shell-dlg-2) MS Sans Serif 또는 Helvetica 대신 합니다. MS Shell Dlg는 대화 상자를 만들기 전에 시스템에서 올바른 글꼴을 사용 하 여 대체 됩니다. MS Shell Dlg 사용 하면이 글꼴을 사용 하 여 처리 하기 위해 운영 체제의 모든 변경 내용을 자동으로 사용할 수 있도록 합니다. (MFC 대체 MS Shell Dlg는 DEFAULT_GUI_FONT 또는 Windows 95, Windows 98 및 Windows NT 4의 시스템 글꼴을 사용 하 여 해당 시스템 MS Shell Dlg를 올바르게 처리 하지 않습니다.)

- 응용 프로그램을 디자인할 때에 문자열을 지역화할 수를 결정 합니다. 확실 하지 않은의 경우 지정 된 문자열을 지역화 될 예정을 가정 합니다. 따라서 작업만 사용 하 여 지역화할 수 있는 문자열을 혼합 하지 마십시오.

## <a name="see-also"></a>참고 항목

[멀티바이트 문자 집합(MBCS) 프로그래밍 팁](../text/mbcs-programming-tips.md)<br/>
[포인터 증가 및 감소](../text/incrementing-and-decrementing-pointers.md)
