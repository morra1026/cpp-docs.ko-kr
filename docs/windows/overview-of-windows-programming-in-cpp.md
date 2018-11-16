---
title: C++의 Windows 프로그래밍 개요
ms.date: 11/15/2018
ms.assetid: efc691d7-21f3-47ae-ae56-cab999ccf59d
ms.openlocfilehash: b33236df6e4c7f679ff1dd9f9f8bc409c86e011a
ms.sourcegitcommit: b032daf81cb5fdb1f5a988277ee30201441c4945
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51693864"
---
# <a name="overview-of-windows-programming-in-c"></a>C++의 Windows 프로그래밍 개요

c + +를 사용 하 여 만들 수 있는 Windows 응용 프로그램의 몇 가지 광범위 한 범주가 있습니다. 각각에 자체 프로그래밍 모델 및 Windows 관련 라이브러리 집합이 있지만 그 중 하나에서 c + + 표준 라이브러리 뿐만 아니라 타사 c + + 라이브러리를 사용할 수 있습니다. 

## <a name="command-line-console-applications"></a>명령줄 (콘솔) 응용 프로그램

C + + 콘솔 응용 프로그램 콘솔 창에 명령줄에서 실행 하 고 텍스트 출력 으로만 표시할 수 있습니다. 자세한 내용은 [콘솔 응용 프로그램](console-applications-in-visual-cpp.md)합니다.
 
## <a name="native-desktop-client-applications"></a>네이티브 데스크톱 클라이언트 응용 프로그램

용어 *데스크톱 네이티브 클라이언트 응용 프로그램* C 또는 c + + 기간 이동 하는 응용 프로그램 원본 Windows Win32 Api를 사용 하 여 액세스 운영 체제를 가리킵니다. 이러한 Api는 주로 C로 작성 된 자체 운영 체제 이벤트를 처리 하는 C 스타일 메시지 루프에 대해 직접 프로그래밍 또는 사용 하 여 선택할 수 있습니다이 종류의 응용 프로그램을 만들 때 *Microsoft Foundation Classes* (MFC), Win32를 래핑하는 c + + 라이브러리 방식 다소 개체 지향입니다. 두 접근 방식에는 "최신" 유니버설 Windows 플랫폼 (아래 참조) 비교할 수 있지만 모두 여전히 완전히 지원 되며 현재 환경에서 실행 되는 코드의 줄에 수백만 개의으로 간주 됩니다.

기존의 Windows c + + 프로그래밍을 사용 하 여 시작을 참조 하세요 [Win32 및 c + + 시작](/windows/desktop/LearnWin32/learn-to-program-for-windows)합니다. Win32 이해를 확보 한 후 더 쉽게 수에 대해 자세히 알아보려면 [MFC Desktop Applications](/mfc/mfc-desktop-applications)합니다. 기존 c + + 데스크톱 응용 프로그램의 정교한 그래픽을 사용 하는 예제를 보려면 [Hilo: Windows에 대 한 c + + 응용 프로그램 개발](https://msdn.microsoft.com/library/windows/desktop/ff708696.aspx)합니다.

### <a name="c-or-net"></a>C + + 또는.NET? 

대부분의 데스크톱 응용 프로그램 시나리오 (즉, 타기 팅 하지 UWP)를 사용 하는 것이 좋습니다 C# 및.NET. 이.NET 프로그래밍은 덜 복잡 한 일반적으로 적으며 오류 발생률, Win32 또는 MFC 보다 더 최신 개체 지향 api 때문입니다. 대부분의 경우, 해당 성능 보다 더 적합합니다. .NET 기능을 풍부한 그래픽에 대 한 Windows Presentation Foundation (WPF) 및 Win32 뿐만 아니라 (UWP 아래 참조)는 최신 Windows 런타임 API 사용할 수 있습니다. 일반적으로 필요한 경우 데스크톱 응용 프로그램에 대 한 c + +를 사용 하는 것이 좋습니다.

- 메모리 사용량 정밀 하 게 제어
- 전력 소비가 가장 경제적
- 일반 컴퓨팅을 위한 GPU 사용
- DirectX에 대 한 액세스
- 표준 c + + 라이브러리의 사용량이

## <a name="com-components"></a>COM 구성 요소

Windows 운영 체제의 많은 부분에서 구성 요소 개체 모델 (COM) 구성 요소를 모든 컴퓨터 언어로 작성 된 클라이언트 응용 프로그램에서 사용할 수 있도록 하는 이진 표준을 정의 하는 기반 합니다. C + +에서 COM 구성 요소를 만드는 작업을 간소화 하기 위해 액티브 템플릿 라이브러리 (ATL)를 사용할 수 있습니다. 자세한 내용은 [구성 요소 개체 모델 (COM)](/windows/desktop/com/component-object-model--com--portal) 하 고 [ATL COM 데스크톱 구성 요소](../atl/atl-com-desktop-components.md)합니다.

## <a name="windows-universal-apps"></a>Windows 유니버설 앱

유니버설 Windows 플랫폼 (UWP)는 최신 Windows API입니다. UWP 앱에 모든 Windows 10 장치에서 실행, XAML을 사용 하 여 사용자 인터페이스에 대 한 및 터치를 완벽 하 게 사용 됩니다. UWP에 대 한 자세한 내용은 참조 하세요. [유니버설 Windows 플랫폼 (UWP) 앱 이란?](/windows/uwp/get-started/whats-a-uwp) 하 고 [Windows 유니버설 앱 가이드](/windows/uwp/get-started/universal-application-platform-guide)합니다.

UWP에 대 한 원래 c + + 지원 구성의 (1) C + + /CX에서는 언어 구문 확장을 사용 하 여 c + + 또는 c + + 표준과 COM.를 기반으로 하는 (2) Windows 런타임 라이브러리 (WRL) C + + /CX 및 WRL은 계속 지원 합니다. 새 프로젝트에 대 한 것이 좋습니다 [C + + /cli WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) 완전히 표준 c + +에 기반 하며 더 빠른 성능을 제공 합니다. 

Windows 10 용으로 기존 c + + 데스크톱 응용 프로그램을 패키지할 수 있습니다-Microsoft Store 통해 배포 합니다. 자세한 내용은 [데스크톱 응용 프로그램 (데스크톱 브리지) 패키지](/windows/uwp/porting/desktop-to-uwp-root)합니다.

## <a name="games"></a>게임

DirectX 게임은 PC 또는 Xbox에서 실행할 수 있습니다. 자세한 내용은 [DirectX Graphics and Gaming](/windows/desktop/directx)합니다.

## <a name="net-wrappers-for-c-libraries"></a>C + + 라이브러리에 대 한.NET 래퍼

에서는 C + +.NET 코드를 네이티브 c + + 라이브러리를 사용할 수 있도록 하는 interop 계층을 만드는 CLI입니다. 자세한 내용은 [.NET 프로그래밍을 사용 하 여 C + + /cli CLI](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)합니다.

## <a name="sql-server-database-clients"></a>SQL Server 데이터베이스 클라이언트

네이티브 코드에서 SQL Server 데이터베이스에 액세스 하려면 ODBC 또는 OLE DB를 사용 합니다. 자세한 내용은 [SQL Server Native Client](/sql/relational-databases/native-client/odbc/sql-server-native-client-odbc)를 참조하세요.

## <a name="windows-device-drivers"></a>Windows 장치 드라이버

드라이버는 하드웨어 장치에서 데이터를 응용 프로그램에 액세스할 수 있도록 하는 하위 수준 구성 요소 및 다른 운영 체제 구성 요소입니다. 자세한 내용은 [Windows Driver Kit (WDK)](/windows-hardware/drivers/index)합니다.

## <a name="windows-services"></a>Windows 서비스

Windows *서비스* 는 거의 또는 전혀 사용자 상호 작용을 사용 하 여 백그라운드에서 실행할 수 있는 프로그램입니다. 이러한 unix에서 이라고 *디먼*합니다. 자세한 내용은 [Services](/windows/desktop/services/services)합니다.

## <a name="sdks-libraries-and-header-files"></a>Sdk, 라이브러리 및 헤더 파일

Visual Studio C 런타임 라이브러리 (CRT), c + + 표준 라이브러리 및 기타 Microsoft 전용 라이브러리를 포함합니다. 이러한 라이브러리에 대 한 헤더 파일이 포함 된 포함 폴더는 \VC\ 폴더 아래에서 또는 Windows SDK 설치 폴더에서 CRT의 경우 Visual Studio 설치 디렉터리에서.

사용할 수는 [Vcpkg 패키지 관리자](../vcpkg.md) 편리 하 게 Windows에 대 한 수백 개의 타사 오픈 소스 라이브러리를 설치 합니다.

Microsoft 라이브러리는 다음과 같습니다.

- MFC(Microsoft Foundation Class): 단추, 목록 상자, 트리 뷰 및 기타 컨트롤이 있는 다양한 기능의 사용자 인터페이스가 있는 일반적인 Windows 프로그램, 특히 엔터프라이즈 응용 프로그램을 만들기 위한 개체 지향 프레임워크입니다. 자세한 내용은 [MFC Desktop Applications](../mfc/mfc-desktop-applications.md)을 참조하세요.

- ATL(Active Template Library): COM 구성 요소를 만들기 위한 강력한 도우미 라이브러리입니다. 자세한 내용은 [ATL COM Desktop Components](../atl/atl-com-desktop-components.md)을 참조하세요.

- C++ AMP(C++ Accelerated Massive Parallelism): GPU에서 고성능 일반 계산 작업에 사용할 수 있는 라이브러리입니다. 자세한 내용은 [C++ AMP (C++ Accelerated Massive Parallelism)](../parallel/amp/cpp-amp-cpp-accelerated-massive-parallelism.md)을 참조하세요.

- 동시성 런타임: 다중 코어 및 다중 코어 장치에 대한 병렬 및 비동기 프로그래밍 작업을 간소화하는 라이브러리입니다. 자세한 내용은 [Concurrency Runtime](../parallel/concrt/concurrency-runtime.md)을 참조하세요.

많은 Windows 프로그래밍 시나리오에는 Windows 운영 체제 구성 요소에 액세스할 수 있는 헤더 파일을 포함하는 Windows SDK도 필요합니다. 기본적으로 Visual Studio는 유니버설 Windows 앱을 개발할 수 있도록 하는 c + + 데스크톱 워크 로드의 구성 요소로 Windows SDK를 설치 합니다. UWP 앱을 개발 하려면 Windows 10 버전의 Windows SDK를 해야 합니다. 정보를 참조 하세요 [Windows 10 SDK](https://dev.windows.com/downloads/windows-10-sdk)합니다. (이전 버전 Windows의 Windows Sdk에 대 한 자세한 내용은 참조는 [Windows SDK 아카이브](https://developer.microsoft.com/windows/downloads/sdk-archive)).

**프로그램 파일 (x86) \Windows 키트** 설치 된 Windows SDK의 모든 버전에 대 한 기본 위치입니다.

Xbox, Azure 등 다른 플랫폼은 설치가 필요한 고유의 SDK가 있습니다. 자세한 내용은 DirectX 개발자 센터 및 Azure 개발자 센터를 참조하세요.

## <a name="development-tools"></a>개발 도구

Visual Studio는 네이티브 코드에 대한 강력한 디버거, 정적 분석 도구, 그래픽 디버깅 도구, 완벽한 기능을 갖춘 코드 편집기, 유닛 테스트 지원 및 다른 많은 도구와 유틸리티를 포함합니다. 자세한 내용은 [Visual Studio를 사용 하 여 개발 시작 하기](/visualstudio/ide/get-started-developing-with-visual-studio), 및 [IDE 및 개발 도구](../ide/ide-and-tools-for-visual-cpp-development.md)합니다.

## <a name="in-this-section"></a>단원 내용
|제목|설명|
|-----------|-----------------|
|[C++의 Windows 데스크톱 응용 프로그램](desktop-applications-visual-cpp.md)| 기존 데스크톱 응용 프로그램을 만드는 방법입니다.|
|[ATL(액티브 템플릿 라이브러리)](../atl/TOC.md)|C + +에서 COM 구성 요소를 만들려면 ATL 라이브러리를 사용 합니다.|
|[MFC(Microsoft Foundation Class)](../mfc/TOC.md)|MFC를 사용 하 여 대화 상자 및 컨트롤을 사용 하 여 크고 작은 Windows 응용 프로그램을 만들려면|
|[ATL 및 MFC 공유 클래스](../atl-mfc-shared/TOC.md)|CString 같은 ATL 및 MFC에서 공유 하는 클래스를 사용 합니다.|
|[C++/CLI를 사용한 .NET 개발](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)|.NET 응용 프로그램 및 구성 요소와의 통신에 사용 하도록 설정 하는 네이티브 c + + 라이브러리에 대 한 래퍼를 만듭니다.|
|[.NET 및 UWP용 구성 요소 확장](component-extensions-for-runtime-platforms.md)|C +에서 공유 하는 구문 요소에 대 한 참조 + /CX 및 C + + /cli CLI입니다.|
|[유니버설 Windows 앱(C++)](universal-windows-apps-cpp.md)|쓰기 UWP 응용 프로그램을 사용 하 여 C + + /CX 또는 Windows 런타임 템플릿 라이브러리 (WRL).|
|[COM 및 .NET에 대한 C++ 특성](attributes/cpp-attributes-com-net.md)|.NET 또는 COM.를 사용 하 여 Windows 전용 프로그래밍에 대 한 비표준 특성|

## <a name="related-articles"></a>관련 문서

|제목|설명|
|-----------|-----------------|
|[Visual C++](../visual-cpp-in-visual-studio.md)|Visual c + + 개발자 콘텐츠에 대 한 부모 항목입니다.|
