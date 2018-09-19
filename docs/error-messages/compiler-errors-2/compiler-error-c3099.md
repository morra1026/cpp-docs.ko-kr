---
title: 컴파일러 오류 C3099 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3099
dev_langs:
- C++
helpviewer_keywords:
- C3099
ms.assetid: b3dded0f-76c9-42c1-991b-532eb8619661
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c5f11e049965fb7374a2294e813502d1279f9f26
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067417"
---
# <a name="compiler-error-c3099"></a>컴파일러 오류 C3099

'keyword': 관리되는 특성에 대해 [System::AttributeUsageAttribute]를 사용하고, WinRT 특성에 대해 [Windows::Foundation::Metadata::AttributeUsageAttribute]를 사용합니다.

사용 하 여 <xref:System.AttributeUsageAttribute> 선언 **/clr** 특성입니다. `Windows::Foundation::Metadata::AttributeUsageAttribute`를 사용하여 Windows 런타임 특성을 선언합니다.

/CLR 특성에 대 한 자세한 내용은 참조 하십시오 [사용자 정의 특성](../../windows/user-defined-attributes-cpp-component-extensions.md)합니다. Windows 런타임에서 지원 되는 특성을 참조 하세요. [Windows.Foundation.Metadata 네임 스페이스](https://msdn.microsoft.com/library/windows/apps/windows.foundation.metadata.aspx)

## <a name="example"></a>예제

다음 샘플에서는 C3099 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C3099.cpp
// compile with: /clr /c
using namespace System;
[usage(10)]   // C3099
// try the following line instead
// [AttributeUsageAttribute(AttributeTargets::All)]
ref class A : Attribute {};
```