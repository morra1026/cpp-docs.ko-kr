---
title: 혼합형, 순수형 및 안정형 기능 비교 (C + + /cli CLI)
ms.date: 11/04/2016
helpviewer_keywords:
- safe assemblies [C++], vs. pure
- mixed assemblies [C++], vs. pure
- safe assemblies [C++], vs. mixed
- pure MSIL [C++]
- verifiable assemblies [C++]
- pure MSIL [C++], vs. safe
- pure MSIL [C++], vs. mixed
- pure MSIL [C++], compared to mixed and safe
- verifiable assemblies [C++], vs. mixed
- mixed assemblies [C++], vs. safe
- verifiable assemblies [C++], vs. pure
- pure assemblies [C++]
- safe assemblies [C++]
- mixed assemblies [C++]
ms.assetid: 3f7a82ba-0e69-4927-ba0c-fbc3160e4394
ms.openlocfilehash: 81fcf986ee68f5f8f64c8070bb992fa1cda1683b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50482074"
---
# <a name="mixed-pure-and-verifiable-feature-comparison-ccli"></a>혼합형, 순수형 및 안정형 기능 비교 (C + + /cli CLI)

이 항목에서는 다양 한 간에 기능 비교 **/clr** 컴파일 모드입니다. 자세한 내용은 [/clr(공용 언어 런타임 컴파일)](../build/reference/clr-common-language-runtime-compilation.md)을 참조하세요.

> [!IMPORTANT]
> **/clr: pure** 및 **/clr: safe** Visual Studio 2015에서 사용 되지 않고 Visual Studio 2017에서 지원 되지 않는 컴파일러 옵션입니다.

## <a name="feature-comparison"></a>기능 비교

|기능|혼합 (/ clr)|순수 (/ clr: pure)|안전 하 게 (/: safe)|관련된 정보|
|-------------|---------------------|-------------------------|-------------------------|-------------------------|
|CRT 라이브러리|지원|deprecated||[범주별 유버니설 C 런타임 루틴](../c-runtime-library/run-time-routines-by-category.md)|
|MFC/ATL|지원|||[MFC 데스크톱 응용 프로그램](../mfc/mfc-desktop-applications.md) &#124; [클래스 개요](../atl/atl-class-overview.md)|
|관리 되지 않는 함수|지원|||[혼합형(네이티브 및 관리) 어셈블리](../dotnet/mixed-native-and-managed-assemblies.md)|
|관리 되지 않는 데이터|지원|deprecated||[순수형 및 안정형 코드(C++/CLI)](../dotnet/pure-and-verifiable-code-cpp-cli.md)|
|관리 되지 않는 함수에서 호출할 수|지원||||
|관리 되지 않는 함수를 호출 하는 지원|지원|deprecated|deprecated|[C++ Interop 사용(암시적 PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)|
|리플렉션을 지원합니다|Dll만|deprecated|deprecated|[리플렉션(C++/CLI)](../dotnet/reflection-cpp-cli.md)|

## <a name="see-also"></a>참고자료

- [순수형 및 안정형 코드(C++/CLI)](../dotnet/pure-and-verifiable-code-cpp-cli.md)