---
title: 값 형식 및 동작 (C + + /cli CLI) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- value types
ms.assetid: 5cb872a6-1e0a-429d-853d-df4ab47e8f2a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 4d2d980e48a6f948c35faf0c4e42969795ef8dc7
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46404659"
---
# <a name="value-types-and-their-behaviors-ccli"></a>값 형식 및 동작(C++/CLI)

값 형식의 Visual c + + c + +에 대 한 Managed Extensions에서 다양 한 방법으로 변경 되었습니다. 이 섹션에서는 CLR 열거형 형식 및 값 클래스 형식 boxing 및 CLR 힙에 boxed 인스턴스에 대 한 액세스 뿐만 아니라 내부 및 고정 포인터 살펴보겠습니다 함께 살펴봅니다. 이 영역에서 광범위 한 언어 변경 되었습니다.

## <a name="in-this-section"></a>섹션 내용

[CLR 열거형 형식](../dotnet/value-types-and-their-behaviors-cpp-cli.md)<br/>
선언 및 열거형의 동작 변경 내용에 설명 합니다.

[값 형식 명시적 boxing](../dotnet/implicit-boxing-of-value-types.md)<br/>
암시적 boxing 값 형식 및 그에 따른 변경 된 동작의 이유를 설명합니다.

[boxed 값에 대한 추적 핸들](../dotnet/a-tracking-handle-to-a-boxed-value.md)<br/>
설명 하는 방법을 암시적 boxing 값 형식이 boxed 값 개체에 대 한 추적 핸들을 변환 합니다.

[값 형식 의미](../dotnet/value-type-semantics.md)<br/>
값 형식 의미 체계를 고정 포인터 및 상속 된 가상 메서드, 클래스 기본 생성자, 내부 포인터를 포함 하 여 변경 내용을 설명 합니다.

## <a name="see-also"></a>참고 항목

[C++/CLI 마이그레이션 입문](../dotnet/cpp-cli-migration-primer.md)<br/>
[클래스 및 구조체](../windows/classes-and-structs-cpp-component-extensions.md)