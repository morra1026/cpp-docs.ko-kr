---
title: 컴파일러 경고 (수준 4) C4571 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4571
dev_langs:
- C++
helpviewer_keywords:
- C4571
ms.assetid: 07aa17bd-b15c-4266-824c-57cc445e8edd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1291466ffd9071929194ffbe7795addfec62eb27
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46088321"
---
# <a name="compiler-warning-level-4-c4571"></a>컴파일러 경고(수준 4) C4571

Visual c + + 7.1; 변경 알림:부터 의미 체계 구조적된 예외 (SEH) 변경 되었습니다.

로 컴파일하는 경우 모든부터 블록에 대해 생성 되는 C4571 **/EHs**합니다.

사용 하 여 컴파일하면 **/EHs**부터 블록은 구조적된 예외 (예: null 포인터를 0으로 나누기)부터 차단 됩니다만 catch 명시적으로 throw 된 c + + 예외를 catch 하지 않습니다.  자세한 내용은 [예외 처리](../../cpp/exception-handling-in-visual-cpp.md)를 참조하세요.

기본적으로 이 경고는 해제되어 있습니다.  이 경고가 표시 되도록 사용 하 여 컴파일하면 **/EHs** 구조적된 예외를 catch 하지 않으려는 사용자 (...) catch 블록입니다.  자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

다음 방법 중 하나를 C4571를 해결할 수 있습니다.

- 사용 하 여 컴파일하면 **/EHa** 구조화 된 예외를 catch 하 여 catch (...) 블록을 계속 하려는 경우.

- 구조화 된 예외를 catch 하 여부터 블록을 원하지 않는 하지만 블록을 사용 하려는 경우에 C4571를 사용 하지 마십시오.  여전히 구조적된 예외 처리 키워드를 사용 하 여 구조화 된 예외를 catch 할 수 있습니다 (**__try**하십시오 **__except**, 및 **__finally**).  하지만 기억를 컴파일하면 **/EHs** 소멸자 SEH 예외가 발생할 때가 아니라 c + + 예외를 throw 될 때에 호출할 수 있습니다.

- 특정 c + + 예외에 대 한 catch 블록을 사용 하 여 catch (...) 블록을 바꾸고 필요에 따라 구조적된 예외 처리는 c + + 예외 처리를 추가 (**__try**하십시오 **__except**, 및 **_ _finally**).  참조 [구조적 예외 처리 (C/c + +)](../../cpp/structured-exception-handling-c-cpp.md) 자세한 내용은 합니다.

참조 [/EH (예외 처리 모델)](../../build/reference/eh-exception-handling-model.md) 자세한 내용은 합니다.

## <a name="example"></a>예제

다음 샘플 C4571를 생성합니다.

```
// C4571.cpp
// compile with: /EHs /W4 /c
#pragma warning(default : 4571)
int main() {
   try {
      int i = 0, j = 1;
      j /= i;   // this will throw a SE (divide by zero)
   }
   catch(...) {}   // C4571 warning
}
```