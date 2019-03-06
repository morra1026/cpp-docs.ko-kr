---
title: 일반 클래스 디자인 원칙
ms.date: 11/04/2016
f1_keywords:
- vc.classes.mfc
helpviewer_keywords:
- designing classes [MFC]
- MFC, Windows API
- Visual C, Windows API calls
- classes [MFC], MFC class design
- Windows API [MFC], and MFC
ms.assetid: e6861ae0-1581-4d9c-9ddf-63f9afcdb913
ms.openlocfilehash: 4dfa11c73703f5f2d3d17f8278610d32178af679
ms.sourcegitcommit: c3093251193944840e3d0a068ecc30e6449624ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57295081"
---
# <a name="general-class-design-philosophy"></a>일반 클래스 디자인 원칙

Microsoft Windows는 c + + 언어 대중화 해지기 전에 설계 되었습니다. 수천 개의 응용 프로그램의 C 언어 Windows API (응용 프로그래밍 인터페이스)를 사용 하므로 해당 인터페이스는 당분간 유지 됩니다. 따라서 모든 c + + Windows 인터페이스를 절차적 C 언어 API를 기반으로 빌드해야 합니다. 이렇게 하면 c + + 응용 프로그램 C 응용 프로그램과 함께 사용 하는 일을 할 수는 있습니다.

Microsoft Foundation Class 라이브러리는 다음과 같은 설계 목표를 충족 하는 Windows에 대 한 개체 지향 인터페이스:

- Windows에 대 한 응용 프로그램을 작성 하기 위해에서 상당히 감소 합니다.

- 실행 속도에 필적할 만한 C 언어 API입니다.

- 최소 코드 크기 오버 헤드입니다.

- 모든 Windows C 함수를 직접 호출할 수 있습니다.

- 기존 C 응용 프로그램을 c + +로 쉽게 변환 합니다.

- 프로그래밍 경험이 풍부한 C 언어 Windows의 기존 자료에서 활용할 수 있습니다.

- 3.를 사용 하 여 보다 c + +를 사용 하 여 Windows API를 쉽게 사용할 수 있도록

- ActiveX 컨트롤, 데이터베이스 지원, 인쇄, 도구 모음 및 상태 표시줄과 같은 기능에 사용 하 여 아직의 강력한 추상화를 쉽게 복잡합니다.

- C + + 언어 기능을 효과적으로 사용 하는 c + +에 대 한 Windows API true입니다.

대 한 자세한 내용은 MFC 라이브러리의 디자인을 참조 하세요.

- [응용 프로그램 프레임 워크](../mfc/application-framework.md)

- [C 언어 API와의 관계](../mfc/relationship-to-the-c-language-api.md)

## <a name="see-also"></a>참고자료

[클래스 개요](../mfc/class-library-overview.md)
