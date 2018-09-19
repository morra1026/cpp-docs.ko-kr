---
title: 컴파일러 경고 (수준 1) C4692 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4692
dev_langs:
- C++
helpviewer_keywords:
- C4692
ms.assetid: f6fb3acc-8228-491a-9c30-ce302d8a9c75
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 691be92230341d0cbf83b361310de4aab60f6859
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46117740"
---
# <a name="compiler-warning-level-1-c4692"></a>컴파일러 경고(수준 1) C4692

'function': 전용이 아닌 멤버의 시그니처에 어셈블리 전용 네이티브 형식 'native_type'이(가) 있습니다.

어셈블리 외부에 표시 된 형식 어셈블리 외부에 표시 되지 않는 네이티브 형식이 포함 된 시그니처는 멤버 함수를 포함 합니다. 따라서 포함 하는 형식 어셈블리 외부에서 인스턴스화된 경우 멤버 함수가 호출 되지 해야 합니다.

자세한 내용은 [표시 유형 입력](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md#BKMK_Type_visibility)합니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [Compiler Warnings That Are Off by Default](../../preprocessor/compiler-warnings-that-are-off-by-default.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플 C4692를 생성합니다.

```
// C4692.cpp
// compile with: /W1 /c /clr
#pragma warning(default:4692)
class Private_Native_Class {};
public class Public_Native_Class {};
public ref class Public_Ref_Class {
public:
   void Test(Private_Native_Class *) {}   // C4692
   void Test2(Public_Native_Class *) {}   // OK
};
```