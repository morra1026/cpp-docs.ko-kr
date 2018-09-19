---
title: 컴파일러 경고 (수준 1) C4165 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4165
dev_langs:
- C++
helpviewer_keywords:
- C4165
ms.assetid: f5bed515-2290-4f88-8dab-b45d95fe26ef
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c532ddee7a2066190c2f926ba7b1240c0418f6c4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46084928"
---
# <a name="compiler-warning-level-1-c4165"></a>컴파일러 경고 (수준 1) C4165

'Bool'; 'HRESULT' 변환 되는 원하는 작업 인지 입니까?

에 HRESULT를 사용 하는 경우는 [경우](../../cpp/if-else-statement-cpp.md) 문을 HRESULT는 변환할 수는 [bool](../../cpp/bool-cpp.md) HRESULT로 변수에 대해 명시적으로 테스트 하지 않은 경우. 기본적으로 이 경고는 해제되어 있습니다.

## <a name="example"></a>예제

다음 샘플에서는 C4165

```cpp
// C4165.cpp
// compile with: /W1
#include <windows.h>
#pragma warning(1:4165)

extern HRESULT hr;
int main() {
   if (hr) {
   // try either of the following ...
   // if (FAILED(hr)) { // C4165 expected
   // if (hr != S_OK) {
   }
}
```