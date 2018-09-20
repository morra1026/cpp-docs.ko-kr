---
title: 관리 되는 형식 (c + +-CL) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- __gc types
- types [C++], CLR
ms.assetid: 1ddd114e-be02-4de7-a4dd-a2d72ad8ff81
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 382228b9e8364d90d7929b4633744071c5eb0c77
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46408042"
---
# <a name="managed-types-ccl"></a>관리되는 형식(C++/CL)

이러한 형식의 개체의 관리 되는 형식 및 생성의 선언 및 사용에 대 한 구문은 크게 변경 되었습니다 Managed Extensions에서 c + + 용 Visual c + +. 이렇게 ISO-C + + 형식 시스템 내에서 통합을 강화 합니다. 이러한 변경 내용은 다음 하위 섹션에 자세히 표시 됩니다.

## <a name="in-this-section"></a>섹션 내용

[관리되는 클래스 형식 선언](../dotnet/declaration-of-a-managed-class-type.md)<br/>
관리 되는 선언 방법에 설명 `class`하십시오 `struct`, 또는 `interface`합니다.

[CLR 참조 클래스 개체 선언](../dotnet/declaration-of-a-clr-reference-class-object.md)<br/>
추적 핸들을 사용 하 여 참조 클래스 형식 개체를 선언 하는 방법을 설명 합니다.

[CLR 배열 선언](../dotnet/declaration-of-a-clr-array.md)<br/>
선언 하 고 배열을 초기화 하는 방법을 설명 합니다.

[생성자 초기화 순서 변경 사항](../dotnet/changes-in-constructor-initialization-order.md)<br/>
클래스 생성자 초기화 순서 키 변경 사항에 설명 합니다.

[소멸자 의미의 변경 내용](../dotnet/changes-in-destructor-semantics.md)<br/>
비 결정적인 종료 설명 `Finalize` 비교 `Dispose`, 참조 개체를 명시적으로 사용 하 여 결과 가져올 `Finalize`합니다.

**참고:** 대리자의 토론은 지연 [대리자 및 이벤트](../dotnet/delegates-and-events.md) 클래스의 일반적인 주제 내의 이벤트 멤버를 사용 하 여 살펴봤듯이 [클래스 또는 인터페이스 내에서 멤버 선언 (C + + /CLI CLI) ](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md).

## <a name="see-also"></a>참고 항목

[C++/CLI 마이그레이션 입문](../dotnet/cpp-cli-migration-primer.md)<br/>
[클래스 및 구조체](../windows/classes-and-structs-cpp-component-extensions.md)<br/>
[배열](../windows/arrays-cpp-component-extensions.md)