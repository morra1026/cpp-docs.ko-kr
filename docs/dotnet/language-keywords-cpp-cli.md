---
title: 언어 키워드 (C + + /cli CLI) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- keywords [C++]
ms.assetid: 021013b2-70ac-4df9-aa77-4af1c67a1a67
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 0b9deb25e203ea805b1430b2ec8e56f17a50123b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46445440"
---
# <a name="language-keywords-ccli"></a>언어 키워드(C++/CLI)

여러 언어 키워드는 Visual c + +에서 Managed Extensions for c + + 변경 합니다.

모든 키워드에서를 접두사로 새 Visual c + + 구문에서는 두 개의 밑줄 제거 됩니다 (한 가지 예외로: `__identifier` 유지 됩니다). 예를 들어 속성이 이제로 선언 `property`이 아니라 `__property`합니다.

Managed Extensions에서 이중 밑줄 접두사를 사용 하기 위한 두 가지 기본 이유가 있었습니다.

- 와 호환 되는 메서드의 로컬 확장명 ISO-C + + 표준을 제공 하는 것입니다. Managed Extensions 디자인의 주요 목표는 토큰 및 new 키워드와 같은 표준 언어와의 비 호환성을 제공 하지 하는 것 이었습니다. 이 따라서 관리 되는 참조 형식 개체의 선언에 대 한 포인터 구문의 선택 된 이유는 상당 부분 있었습니다.

- 해당와 호환 되는 측면 외에도 두 개의 밑줄을 사용 중인 언어 사용자의 기존 코드 베이스를 침해 하지 않는다는 이기도 합니다. 이것은 Managed Extensions 디자인의 두 번째 주요 목표입니다.

두 개의 밑줄 제거에 불구 하 고 Microsoft 방침은 남아 있습니다. 그러나 지원 CLR 동적 개체 모델은 새롭고 강력한 프로그래밍 패러다임을 나타냅니다. 이 새로운 패러다임의 지원에는 자체 고급 키워드 및 토큰 필요합니다. 에서는 표준 언어를 지원 하 고 통합 하는 동안이 새로운 패러다임의 최고 수준의 식 제공 하고자 합니다. 이러한 두 가지 서로 다른 개체 모델의 첫 번째 클래스 프로그래밍 환경을 제공 하는 새로운 구문 디자인 합니다.

마찬가지로,을 이러한 새로운 언어 키워드 무난 기울였습니다 됩니다. 이 상황에 맞는 및 공백이 포함 된 키워드를 사용 하 여 완료 된 했습니다. 실제 새 언어 구문을 살펴봅니다 전에 이러한 두 가지 특수 키워드 종류 이해 하기가 해 보겠습니다.

상황별 키워드는 특정 프로그램 컨텍스트 내에서 특별 한 의미 합니다. 예를 들어 일반 프로그램 내에서 `sealed` 일반 식별자로 처리 됩니다. 그러나 관리 되는 참조 클래스 형식 선언 부분 내에서 발생할 때 해당 클래스 선언 컨텍스트 내에서 키워드로 처리 됩니다. 이 기존 코드 베이스를 사용 하 여 사용자에 게 매우 중요 하다 고 생각 하는 적인 영향을 미칠 것 언어에서 새로운 키워드를 소개 최소화 합니다. 동시에, 최고 수준의 환경을 추가 언어 기능의-Managed Extensions를 사용 하 여 가능한 되지 않는 새로운 기능의 사용자 수 있습니다. 방식의 예로 `sealed` 는 참조 [는 관리 되는 클래스 형식 선언](../dotnet/declaration-of-a-managed-class-type.md)합니다.

공백이 포함 된 키워드와 같은 `value class`, 상황에 맞는 키워드는 특별 한 경우. Existing 키워드를 공백으로 구분 하 여 상황에 맞는 한정자 쌍 것입니다. 쌍은 두 개의 별도 키워드가 아닌 단일 단위로 취급 됩니다.

## <a name="see-also"></a>참고 항목

[C++/CLI 마이그레이션 입문](../dotnet/cpp-cli-migration-primer.md)<br/>
[런타임 플랫폼용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)