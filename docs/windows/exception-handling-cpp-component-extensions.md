---
title: 예외 처리 (C + + /cli 및 C + + /cli CX) | Microsoft Docs
ms.custom: ''
ms.date: 10/12/2018
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- structured exception handling [C++], managed exceptions
- Exception class, managed applications
- exception handling
- C++ exception handling
- exception handling, types of
- System::Exception class in managed applications
ms.assetid: ccb11fe8-6938-41ac-b477-a183e85865b9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7d070cc223f90f84bd52176ee7e50dbbfa441789
ms.sourcegitcommit: 3f4e92266737ecb70507871e87dc8e2965ad7e04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49328131"
---
# <a name="exception-handling--ccli-and-ccx"></a>예외 처리 (C + + /cli 및 C + + /cli CX)

로 컴파일된 응용 프로그램을 `/ZW` 컴파일러 옵션 또는 `/clr` 컴파일러 옵션 둘 다 사용 *예외* 프로그램 실행 중 예기치 않은 오류를 처리 합니다. 다음 항목은 C++/CX 또는 C++/CLI 응용 프로그램 중 하나에서 예외 처리에 대해 설명합니다.

## <a name="in-this-section"></a>섹션 내용

[관리되는 예외 사용의 기본 개념](../dotnet/basic-concepts-in-using-managed-exceptions.md)<br/>
설명 예외를 throw 하 고 사용 하 여 **시도**/**catch** 블록입니다.

[예외 처리 동작에서 /clr 차이점](../dotnet/differences-in-exception-handling-behavior-under-clr.md)<br/>
C++ 예외 처리의 표준 동작과의 차이점을 설명합니다.

[finally](../dotnet/finally.md)<br/>
Finally 키워드를 사용하는 방법을 설명합니다.

[방법: 전역 예외 처리기 정의 및 설치](../dotnet/how-to-define-and-install-a-global-exception-handler.md)<br/>
처리되지 않은 예외를 캡처하는 방법을 보여 줍니다.

[방법: 네이티브 코드에서 MSIL이 throw한 예외 catch](../dotnet/how-to-catch-exceptions-in-native-code-thrown-from-msil.md)<br/>
네이티브 코드에서 CLR 및 C++ 예외를 catch하는 방법을 설명합니다.

[방법: 전역 예외 처리기 정의 및 설치](../dotnet/how-to-define-and-install-a-global-exception-handler.md)<br/>
처리되지 않은 예외를 catch하는 방법을 보여 줍니다.

## <a name="related-sections"></a>관련 단원

[예외 처리](../cpp/exception-handling-in-visual-cpp.md)<br/>
표준 c + +에서 예외를 처리에 대해 설명 합니다.

## <a name="see-also"></a>참고 항목

[.NET 및 UWP 용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)