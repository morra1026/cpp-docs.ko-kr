---
title: 매개 변수 배열 및 가변 매개 변수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- function overloading, argument matching
ms.assetid: 492e3f6c-1c4c-4e0c-a358-72f2d39c30be
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 2caf6415fdbceb506b736e209c6e7e384b567c5a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46384379"
---
# <a name="param-array-and-ellipsis"></a>매개 변수 배열 및 가변 매개 변수(...)

오버 로드 된 함수 호출을 확인 하는 것에 대 한 매개 변수 배열의 우선 순위는 Visual c + + c + +에 대 한 Managed Extensions에서 변경 되었습니다.

Managed Extensions 및 새 구문에서 지 원하는 C# 및 Visual Basic 매개 변수 배열에 대 한 명시적 지원 되지 않습니다 있습니다. 대신 하나 플래그 특성을 사용 하 여 일반 배열 다음과 같습니다.

```
void Trace1( String* format, [ParamArray]Object* args[] );
void Trace2( String* format, Object* args[] );
```

이 둘은 모두 동일 하 게 보이지만 동안는 `ParamArray` 특성 태그이 C# 이나 다른 CLR 언어에 대 한 다양 한 각 호출을 사용 하 여 요소를 수행 하는 배열입니다. Managed Extensions와 새 구문 간의 프로그램에서 동작의 변화를 하나의 인스턴스는 줄임표 (...)를 선언에서 설정 하는 오버 로드 된 함수의 확인이 고 두 번째 선언 된 `ParamArray` 제공한 다음 예제와 같이 특성 Artur Laksberg 합니다.

```
int fx(...); // 1
int fx( [ParamArray] Int32[] ); // 2
```

Managed extensions에서 줄임표 특성 언어의 공식 측면 아니기 때문에 적합 하는 특성을 통해 우선 순위를 제공 되었습니다. 그러나 새 구문에서 매개 변수 배열은 이제 언어 내에서 직접 지원 하 고 줄임표 위로 우선 순위는 더 강력한 형식 때문에 지정 됩니다. Managed Extensions, 호출에 따라서

```
fx( 1, 2 );
```

로 확인 되 `fx(...)` 새 구문에서 확인 된 `ParamArray` 인스턴스. 프로그램 동작에 비해 줄임표 인스턴스 호출에 의존 합니다. 해제 가능성에는 `ParamArray`, 서명 또는 호출을 수정 해야 합니다.

## <a name="see-also"></a>참고 항목

[일반적인 언어 변경 사항(C++/CLI)](../dotnet/general-language-changes-cpp-cli.md)