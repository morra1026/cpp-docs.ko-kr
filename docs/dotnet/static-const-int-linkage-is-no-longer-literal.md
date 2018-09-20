---
title: Static Const Int 링크가 더 이상 리터럴이 아님 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- literal attribute [C++]
- constants, declaring
- integral constant expressions
ms.assetid: d2a5e3d2-ffb0-4b61-8114-bec5993a1195
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: c51853274b061ba290ff90993f45ccdf3375349b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46431296"
---
# <a name="static-const-int-linkage-is-no-longer-literal"></a>Static Const Int 링크가 더 이상 리터럴이 아닙니다.

상수는 클래스 멤버의 선언이 Visual c + + Managed Extensions for c + + 변경 되었습니다.

하지만 `static const` 정수 멤버 여전히 지원 되는 경우 해당 링크 특성이 변경 되었습니다. 이제 이전 링크 특성은 리터럴 정수 멤버에서 수행 됩니다. 예를 들어, 다음 Managed Extensions 클래스를 것이 좋습니다.

```
public __gc class Constants {
public:
   static const int LOG_DEBUG = 4;
};
```

이 필드 (참고 리터럴 특성)에 대 한 다음 기본 CIL 특성을 생성합니다.

```
.field public static literal int32
modopt([Microsoft.VisualC]Microsoft.VisualC.IsConstModifier) STANDARD_CLIENT_PRX = int32(0x00000004)
```

하지만이 새 구문에서 계속 컴파일됩니다.

```
public ref class Constants {
public:
   static const int LOG_DEBUG = 4;
};
```

리터럴 특성을 더 이상 생성 하 고 따라서은 볼 수 없음 상수로 CLR 런타임에서:

```
.field public static int32 modopt([Microsoft.VisualC]Microsoft.VisualC.IsConstModifier) STANDARD_CLIENT_PRX = int32(0x00000004)
```

동일한 언어 간 리터럴 특성을 가지려면 선언을 변경 해야 새로 지원 되 `literal` 같이 데이터 멤버

```
public ref class Constants {
public:
   literal int LOG_DEBUG = 4;
};
```

## <a name="see-also"></a>참고 항목

[클래스 또는 인터페이스 내에서 멤버 선언(C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)<br/>
[리터럴](../windows/literal-cpp-component-extensions.md)