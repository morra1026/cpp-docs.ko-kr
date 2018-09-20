---
title: 클래스 또는 인터페이스 내에서 멤버 선언 (C + + /cli CLI) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- members, declaration syntax
- class members, declaration syntax
ms.assetid: 95d312a4-198b-46f0-b8f5-15253807c55e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 80b872b4c614677c05b0d28b821d3a48255905c5
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46430639"
---
# <a name="member-declarations-within-a-class-or-interface-ccli"></a>클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)

속성 및 연산자 선언에 광범위 하 게 변경 되었습니다 Managed Extensions에서 c + +에 대 한 Visual c + +, Managed Extensions 디자인에서 제공 되었던 내부 구현 세부 정보 숨기기. 이벤트 선언도 수정 되었습니다.

변경의 범주에 있는 정적 생성자 수 이제 Managed Extensions 지원 되지 않습니다 되도록 정의 된 아웃 아웃오브 라인 (관리 되는 확장 내에서 인라인으로 정의 되도록 필수 된 이러한), 및 위임 생성자 개념이 도입 되었습니다.

## <a name="in-this-section"></a>섹션 내용

[속성 선언](../dotnet/property-declaration.md)<br/>
속성 선언에는 변경에 설명 합니다.

[속성 인덱스 선언](../dotnet/property-index-declaration.md)<br/>
인덱싱된 속성 선언에는 변경에 설명 합니다.

[대리자 및 이벤트](../dotnet/delegates-and-events.md)<br/>
대리자 및 이벤트 선언 구문이 변경에 설명 합니다.

[가상 함수 봉인](../dotnet/sealing-a-virtual-function.md)<br/>
함수 봉인 구문을 변경 내용을 설명 합니다.

[오버로드된 연산자](../dotnet/overloaded-operators.md)<br/>
연산자 오버 로드 변경에 설명 합니다.

[변환 연산자의 변경 내용](../dotnet/changes-to-conversion-operators.md)<br/>
변환 연산자의 변경 내용에 설명 합니다.

[인터페이스 멤버 명시적 재정의](../dotnet/explicit-override-of-an-interface-member.md)<br/>
변경 내용을 명시적으로 인터페이스 멤버를 재정의 하는 방법 설명 합니다.

[전용 가상 함수](../dotnet/private-virtual-functions.md)<br/>
개인 가상 함수가 파생된 클래스에서 처리 되는 방식에서 변경에 설명 합니다.

[Static Const Int 링크가 더 이상 리터럴이 아님](../dotnet/static-const-int-linkage-is-no-longer-literal.md)<br/>
방식에서 변경에 설명 `static const` 연결 된 정수 계열 멤버 및 명시적으로 new를 사용 하는 상수를 선언 하는 방법을 `literal` 키워드입니다.

## <a name="see-also"></a>참고 항목

[C++/CLI 마이그레이션 입문](../dotnet/cpp-cli-migration-primer.md)