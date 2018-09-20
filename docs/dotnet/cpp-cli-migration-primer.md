---
title: C + + /cli 마이그레이션 입문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- C++/CLI Version 2
- upgrading Visual C++ applications, Managed Extensions for C++ to Visual C++ 2005 syntax
- migration [C++], C++/CLI Version 2
- Managed Extensions for C++, upgrading syntax
- C++/CLI Version 2, managed extensions
ms.assetid: 8ec926b5-73f6-4f0c-bcdf-5203d293849a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 88b32ea226971c0fa5b6d269a8992629c3c4de77
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46385433"
---
# <a name="ccli-migration-primer"></a>C++/CLI 마이그레이션 입문

Visual c + + 프로그램에서에서 이동 Managed Extensions for c + + Visual c + +에 대 한 지침입니다.

C + + /cli는 ISO-C + + 표준 언어에 동적 구성 요소 프로그래밍 패러다임을 확장 합니다. 새 언어는 Managed Extensions를 통해 다양 한 중요 한 향상 된 기능을 제공합니다. 이 섹션에서는 Visual c + +는 이러한 매핑을 매핑이 존재 하는 구문은 해당 지적 하는 열거 된 목록을 통해 Managed Extensions for c + + 언어 기능 및 매핑과 제공 합니다.

## <a name="in-this-section"></a>섹션 내용

[변경 사항 개요(C++/CLI)](../dotnet/outline-of-changes-cpp-cli.md)<br/>
변경 내용 목록은 아래에 있는 5 개의 일반 범주를 제공 하는 빠른 참조를 간단히 합니다.

[언어 키워드(C++/CLI)](../dotnet/language-keywords-cpp-cli.md)<br/>
두 개의 밑줄 제거 하 고 상황에 맞는 공백이 포함 된 키워드 도입 등의 언어 키워드에 대 한 변경 내용을 설명 합니다.

[관리 되는 형식 (C + + /cli CL)](../dotnet/managed-types-cpp-cl.md)<br/>
구문에서 변경 된 선언의 일반적인 형식 시스템 (CTS)-살펴보고 클래스, 배열 (매개 변수 배열 포함), 열거형 및 등의 선언에 변경 내용이 포함 됩니다.

[클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)<br/>
스칼라 속성, 인덱스 속성, 연산자, 대리자 및 이벤트와 같은 클래스 멤버와 관련 된 변경 내용을 표시 합니다.

[값 형식 및 동작(C++/CLI)](../dotnet/value-types-and-their-behaviors-cpp-cli.md)<br/>
값 형식과 내부 및 고정 포인터의 새로운 패밀리에 초점을 맞춥니다. 또한 암시적 boxing, boxed 값 형식의 불변성 및 값 클래스 내에서 기본 생성자에 대 한 지원 제거와 같은 중요 한 의미 변경에 대해서도 설명 합니다.

[일반적인 언어 변경 사항(C++/CLI)](../dotnet/general-language-changes-cpp-cli.md)<br/>
캐스트 표기법에 대 한 지원과 같은 의미 변경 사항 세부 정보 문자열 리터럴 동작 및 ISO-C + + 및 C + 사이의 의미에서 변경 내용을 + CLI입니다.

## <a name="see-also"></a>참고 항목

[혼합형(네이티브 및 관리) 어셈블리](../dotnet/mixed-native-and-managed-assemblies.md)<br/>
[런타임 플랫폼용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)