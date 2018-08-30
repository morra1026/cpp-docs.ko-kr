---
title: 프로젝트를 변환 혼합 모드 순수 Intermediate Language로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- intermediate language, mixed-mode applications
- mixed-mode applications
- mixed-mode applications, intermediate language
- projects [C++], converting to intermediate language
ms.assetid: 855f9e3c-4f09-4bfe-8eab-a45f68292be9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 263a90710d2103c4ea97e6c56da67d676ba7366b
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43222082"
---
# <a name="converting-projects-from-mixed-mode-to-pure-intermediate-language"></a>혼합된 모드에서 순수 intermediate language로 프로젝트를 변환

모든 Visual c + + CLR 프로젝트는 기본적으로 C 런타임 라이브러리에 연결합니다. 따라서 이러한 프로젝트는 공용 언어 런타임 (관리 코드)를 대상으로 하는 코드를 사용 하 여 네이티브 코드를 결합 하기 때문에 혼합 모드 응용 프로그램으로 분류 됩니다. 컴파일되는 경우 중간 언어 (IL) 라고도 MSIL (Microsoft intermediate language)로 컴파일됩니다.

> [!IMPORTANT]
> 사용 되지 않는 visual Studio 2015 및 Visual Studio 2017은 더 이상 생성을 지원할 **/clr: pure** 또는 **/clr: safe** CLR 응용 프로그램에 대 한 코드입니다. 순수 이미지나 안전 어셈블리를 필요로 하는 경우에 C# 응용 프로그램을 변환 하는 것이 좋습니다.

지 원하는 Visual c + + 컴파일러 도구 집합의 이전 버전을 사용 하는 경우 **/clr: pure** 또는 **/clr: safe**, 순수 MSIL로 코드를 변환 하려면이 절차를 사용할 수 있습니다:

### <a name="to-convert-your-mixed-mode-application-into-pure-intermediate-language"></a>순수 중간 언어로 혼합 모드 응용 프로그램을 변환 하려면

1. 에 대 한 링크를 제거 합니다 [C 런타임 라이브러리](../c-runtime-library/crt-library-features.md) (CRT):

   1. .Cpp 파일에 대 한 진입점 변경 응용 프로그램의 진입점을 정의 `Main()`합니다. 사용 하 여 `Main()` 프로젝트가 CRT에 연결 되지 않습니다 나타냅니다.

   2. 솔루션 탐색기에서 프로젝트를 마우스 오른쪽 단추로 클릭 하 고 선택 **속성** 응용 프로그램에 대 한 속성 페이지를 열려면 바로 가기 메뉴.

   3. **고급** 프로젝트 속성 페이지에 대 한는 **링커**를 선택 합니다 **진입점** 하 고 enter **Main** 이 필드에.

   4. 콘솔 응용 프로그램에 대 한에서 **시스템** 프로젝트 속성 페이지에 대 한는 **링커**를 선택 합니다 **하위 시스템** 필드를 변경 하려면이 옵션 **콘솔 (/ SUBSYSTEM:CONSOLE)** 합니다.

      > [!NOTE]
      > 때문에 Windows Forms 응용 프로그램에 대 한이 속성을 설정할 필요가 없습니다 합니다 **하위 시스템** 필드 설정 됩니다 **Windows (/ 하위 시스템: WINDOWS)** 기본적으로 합니다.

   5. Stdafx.h에서 모든 주석는 `#include` 문입니다. 예를 들어 콘솔 응용 프로그램에서

      ```cpp
      // #include <iostream>
      // #include <tchar.h>
      ```

       또는

       Windows Forms 응용 프로그램의 예를 들어,

      ```cpp
      // #include <stdlib.h>
      // #include <malloc.h>
      // #include <memory.h>
      // #include <tchar.h>
      ```

   6. Windows Forms 응용 프로그램 Form1.cpp 주석으로 처리에 대 한는 `#include` windows.h를 참조 하는 문입니다. 예를 들어:

      ```cpp
      // #include <windows.h>
      ```

2. Stdafx.h에 다음 코드를 추가 합니다.

   ```cpp
   #ifndef __FLTUSED__
   #define __FLTUSED__
      extern "C" __declspec(selectany) int _fltused=1;
   #endif
   ```

3. 모든 관리 되지 않는 형식을 제거 합니다.

   적절 한 위치에서 구조에 대 한 참조를 사용 하 여 관리 되지 않는 형식 대체를 [시스템](https://msdn.microsoft.com/library/system.appdomainmanager.appdomainmanager.aspx) 네임 스페이스입니다. 일반적인 관리 되는 유형이 다음 표에 나와 있습니다.

   |구조체|설명|
   |---------------|-----------------|
   |[Boolean](https://msdn.microsoft.com/library/system.boolean\(v=vs.140\).aspx)|부울 값을 나타냅니다.|
   |[Byte](https://msdn.microsoft.com/library/system.byte\(v=vs.140\).aspx)|부호 없는 8비트 정수를 나타냅니다.|
   |[Char](https://msdn.microsoft.com/library/system.char\(v=vs.140\).aspx)|유니코드 문자를 나타냅니다.|
   |[DateTime](https://msdn.microsoft.com/library/system.datetime.datetime.aspx)|일반적으로 날짜와 시간으로 표시된 시간을 나타냅니다.|
   |[Decimal](https://msdn.microsoft.com/library/system.decimal\(v=vs.140\).aspx)|10진수를 나타냅니다.|
   |[Double](https://msdn.microsoft.com/library/system.double\(v=vs.140\).aspx)|배정밀도 부동 소수점 숫자를 나타냅니다.|
   |[Guid](https://msdn.microsoft.com/library/system.guid\(v=vs.140\).aspx)|GUID(Globally Unique IDentifier)를 나타냅니다.|
   |[Int16](https://msdn.microsoft.com/library/system.int16\(v=vs.140\).aspx)|부호 있는 16비트 정수를 나타냅니다.|
   |[Int32](https://msdn.microsoft.com/library/system.int32\(v=vs.140\).aspx)|부호 있는 32비트 정수를 나타냅니다.|
   |[Int64](https://msdn.microsoft.com/library/system.int64\(v=vs.140\).aspx)|부호 있는 64비트 정수를 나타냅니다.|
   |[IntPtr](https://msdn.microsoft.com/library/system.intptr\(v=vs.140\).aspx)|포인터나 핸들을 나타내는 데 사용되는 플랫폼별 형식입니다.|
   |[SByte](https://msdn.microsoft.com/library/system.byte.aspx)|8비트 부호 있는 정수를 나타냅니다.|
   |[Single](https://msdn.microsoft.com/library/system.single.aspx)|단정밀도 부동 소수점 숫자를 나타냅니다.|
   |[TimeSpan](https://msdn.microsoft.com/library/system.timespan\(v=vs.140\).aspx)|시간 간격을 나타냅니다.|
   |[UInt16](https://msdn.microsoft.com/library/system.uint16\(v=vs.140\).aspx)|16비트 부호 없는 정수를 나타냅니다.|
   |[UInt32](https://msdn.microsoft.com/library/system.uint32\(v=vs.140\).aspx)|32비트 부호 없는 정수를 나타냅니다.|
   |[UInt64](https://msdn.microsoft.com/library/system.uint64\(v=vs.140\).aspx)|64비트 부호 없는 정수를 나타냅니다.|
   |[UIntPtr](https://msdn.microsoft.com/library/system.uintptr\(v=vs.140\).aspx)|포인터나 핸들을 나타내는 데 사용되는 플랫폼별 형식입니다.|
   |[void](https://msdn.microsoft.com/library/system.void\(v=vs.140\).aspx)|값을 반환 하지 않는 메서드를 나타냅니다. 즉, 메서드 void 반환 형식을 갖습니다.|