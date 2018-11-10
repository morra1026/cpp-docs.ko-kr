---
title: 연결 지점 구현(Visual C++)
ms.date: 11/04/2016
helpviewer_keywords:
- Implement Connection Point Wizard [C++]
- connection points [C++], implementing
ms.assetid: 5b37e4f9-73c9-4bef-b26d-365bc0662260
ms.openlocfilehash: 45e3dfcfc7e7bcb9fcbe14e08a8c238fe9bec5a1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50568326"
---
# <a name="implementing-a-connection-point-visual-c"></a>연결 지점 구현(Visual C++)

연결 지점 구현 마법사를 사용하여 연결 지점을 구현하려면 ATL COM 응용 프로그램 또는 ATL 지원이 포함된 MFC 응용 프로그램으로 프로젝트를 만들어야 합니다. [ATL 프로젝트 마법사](../atl/reference/atl-project-wizard.md)를 사용하여 ATL 응용 프로그램을 만들거나 [MFC 응용 프로그램에 ATL 개체를 추가](../mfc/reference/adding-atl-support-to-your-mfc-project.md)하여 MFC 응용 프로그램용 ATL 지원을 구현할 수 있습니다.

> [!NOTE]
>  MFC 프로젝트의 연결 지점 구현에 대한 자세한 내용은 [연결 지점](../mfc/connection-points.md)을 참조하세요.

프로젝트를 생성한 후 연결 지점을 구현하려면 먼저 ATL 개체를 추가해야 합니다. ATL 프로젝트에 개체를 추가하는 마법사 목록은 [ATL 프로젝트에 개체 및 컨트롤 추가](../atl/reference/adding-objects-and-controls-to-an-atl-project.md)를 참조하세요.

> [!NOTE]
>  이 마법사는 ATL 서버, 성능 개체 또는 성능 카운터를 사용하여 만든 XML Web services, ATL 대화 상자를 지원하지 않습니다.

연결 가능한 개체(즉, 원본)는 각 송신 인터페이스에 대한 연결 지점을 노출할 수 있습니다. 각 송신 인터페이스는 클라이언트가 개체(예: 싱크)에 구현할 수 있습니다. 자세한 내용은 [ATL 연결 지점](../atl/atl-connection-points.md)을 참조하세요.

### <a name="to-implement-a-connection-point"></a>연결 지점을 구현하려면

1. 클래스 뷰에서 ATL 개체의 클래스 이름을 마우스 오른쪽 단추로 클릭합니다.

1. 바로 가기 메뉴에서 **추가**를 클릭한 다음, **연결 지점 추가**를 클릭하여 [연결 지점 구현 마법사](../ide/implement-connection-point-wizard.md)를 표시합니다.

1. 적절한 형식 라이브러리에서 구현할 연결 지점 인터페이스를 선택하고 **마침**을 클릭합니다.

1. 클래스 뷰에서 각 연결 지점에 대해 생성된 프록시 클래스를 검사합니다. 클래스는 CProxy*InterfaceName*\<T>로 나타나며 [IConnectionPointImpl](../atl/reference/iconnectionpointimpl-class.md)에서 파생됩니다.

1. 연결 지점 클래스를 두 번 클릭하여 연결 지점 클래스의 정의를 표시합니다.

   - 사용자 고유의 프로젝트 인터페이스에 대한 연결 지점을 구현하는 경우 다음 정의가 나타납니다.

        ```
        template< class T >
        class CProxyInterfaceName :
           public IConnectionPointImpl< T, &IID_InterfaceName >
        {
        public:
        };
        ```

         If you implement a local interface, methods and properties appear in the class body.

   - 다른 인터페이스의 연결 지점을 구현하는 경우 각각 이름이 `Fire_`로 시작하는 인터페이스의 메서드가 정의에 포함됩니다.

## <a name="see-also"></a>참고 항목

[코드 마법사로 기능 추가](../ide/adding-functionality-with-code-wizards-cpp.md)<br>
[개체에 연결 지점 추가](../atl/adding-connection-points-to-an-object.md)