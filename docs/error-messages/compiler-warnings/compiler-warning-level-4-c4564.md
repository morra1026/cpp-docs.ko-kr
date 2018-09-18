---
title: 컴파일러 경고 (수준 4) C4564 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4564
dev_langs:
- C++
helpviewer_keywords:
- C4564
ms.assetid: 555b301b-313e-4262-9f81-eb878674be60
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ea8d392251c8168490d7841ad590731b5a08e7f5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46031836"
---
# <a name="compiler-warning-level-4-c4564"></a>컴파일러 경고(수준 4) C4564

' method' 'class' 클래스의 지원 되지 않는 기본 매개 변수 'parameter'를 정의합니다.

컴파일러는 기본값을 사용 하 여 하나 이상의 매개 변수를 사용 하 여 메서드를 발견 했습니다. 메서드가 호출 된; 경우 매개 변수의 기본 값이 무시 됩니다. 이러한 매개 변수 값을 명시적으로 지정 합니다. 이러한 매개 변수 값을 명시적으로 지정 하지 않으면 c + + 컴파일러 오류가 발생 합니다.

Visual Basic을 사용 하 여 만든 다음.dll, 지정 된에서 허용 하는 기본 매개 변수 메서드 인수:

```
' C4564.vb
' compile with: vbc /t:library C4564.vb
Public class TestClass
   Public Sub MyMethod (a as Integer, _
                        Optional c as Integer=1)
   End Sub
End class
```

및 Visual Basic을 사용 하 여 만든.dll을 사용 하는 다음 c + + 샘플

```
// C4564.cpp
// compile with: /clr /W4 /WX
#using <C4564.dll>

int main() {
   TestClass ^ myx = gcnew TestClass();   // C4564
   myx->MyMethod(9);
   // try the following line instead, to avoid an error
   // myx->MyMethod(9, 1);
}
```