---
title: 컴파일러 경고(수준 4) C4289
ms.date: 11/04/2016
f1_keywords:
- C4289
helpviewer_keywords:
- C4289
ms.assetid: 0dbd2863-4cde-4e16-894b-104a2d5fa724
ms.openlocfilehash: 3a997af466ddfdaaf4631afeb53d917ce0338c3b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50488814"
---
# <a name="compiler-warning-level-4-c4289"></a>컴파일러 경고(수준 4) C4289

비표준 확장이 사용됨 : 'var' : for 루프에서 선언된 루프 제어 변수가 for 루프 범위 외부에서 사용되었습니다.

로 컴파일하는 경우 [/Ze](../../build/reference/za-ze-disable-language-extensions.md) 및 **/zc: forscope-** 에 선언 된 변수를 [에 대 한](../../cpp/for-statement-cpp.md) 루프 된 후 사용 하는 **에 대 한**-루프 범위.

참조 [/zc: forscope](../../build/reference/zc-forscope-force-conformance-in-for-loop-scope.md) 의 표준 동작을 지정 하는 방법에 대 한 내용은 **에 대 한** 루프 **/Ze**합니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

다음 샘플에서는 C4289 오류가 생성 됩니다.

```
// C4289.cpp
// compile with: /W4 /Zc:forScope-
#pragma warning(default:4289)
int main() {
   for (int i = 0 ; ; )   // C4289
      break;
   i++;
}
```