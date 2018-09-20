---
title: 일반적인 언어 변경 사항 (C + + /cli CLI) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 79a70768-225c-4ae2-84d1-178b20a9b042
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 9b48ebdf0bf25399b08f8a1cb1240a857cfad352
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46418465"
---
# <a name="general-language-changes-ccli"></a>일반적인 언어 변경 사항(C++/CLI)

CLR 언어 기능을 Visual c + +에서 Managed Extensions for c + + 변경 수입니다.

이 섹션에 설명 된 내용이 여러 언어의 정렬 합니다. 문자열 리터럴, 줄임표 사이의 오버 로드 확인의 변경 처리에서 변경을 포함 하며 `Param` 특성을 변경 하 여 `typeof` 에 `typeid`, 생성자 이니셜라이저 목록에서의 호출을 변경 및 새 캐스트 표기법에 도입 된 `safe_cast`합니다.

[문자열 리터럴](../dotnet/string-literal.md)<br/>
문자열 리터럴의 처리에 변경 하는 방법을 설명 합니다.

[매개 변수 배열 및 가변 매개 변수(...)](../dotnet/param-array-and-ellipsis.md)<br/>
에 대해 설명 하는 방법 `ParamArray` 가변 매개 변수 보다 우선 순위가 이제 높습니다 (`...`) 다양 한 개수의 인수를 사용 하 여 함수 호출을 확인 하는 것에 대 한 합니다.

[typeof 대신 T::typeid 사용](../dotnet/typeof-goes-to-t-typeid.md)<br/>
에 대해 설명 하는 방법을 `typeof` 연산자로 변경 된가 데 `typeid`합니다.

[이니셜라이저 목록](../dotnet/initializer-lists.md)<br/>
이니셜라이저 목록의 호출 순서 변경 사항에 설명 합니다.

[캐스트 표기법 및 safe_cast<> 도입](../dotnet/cast-notation-and-introduction-of-safe-cast-angles.md)<br/>
캐스트 표기법 및 특정 변경 내용을 도입에 설명 `safe_cast`합니다.

## <a name="see-also"></a>참고 항목

[C++/CLI 마이그레이션 입문](../dotnet/cpp-cli-migration-primer.md)