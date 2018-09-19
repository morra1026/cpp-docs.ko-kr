---
title: 컴파일러 오류 C3899 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3899
dev_langs:
- C++
helpviewer_keywords:
- C3899
ms.assetid: 14e07e4a-f7a7-4309-baaa-649d69e12e23
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b154941051e1c6887e8e05756befd6a18c62ed72
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46091785"
---
# <a name="compiler-error-c3899"></a>컴파일러 오류 C3899

'var': 'class' 클래스의 병렬 영역 내부에서는 직접 initonly 데이터 멤버의 값 (l-value)-사용 되지

[initonly (C + + /cli CLI)](../../dotnet/initonly-cpp-cli.md) 내에 있는 생성자의 해당 부분에서 데이터 멤버를 초기화할 수 없습니다는 [병렬](../../parallel/openmp/reference/parallel.md) 지역입니다.  더 효과적으로 이상 생성자의 일부가 되도록 컴파일러는 해당 코드의 내부를 재배치 때문입니다.

를 해결 하려면 생성자에서 있지만 병렬 영역 밖에 initonly 데이터 멤버를 초기화 합니다.

## <a name="example"></a>예제

다음 샘플 C3899를 생성합니다.

```
// C3899.cpp
// compile with: /clr /openmp
#include <omp.h>

public ref struct R {
   initonly int x;
   R() {
      x = omp_get_thread_num() + 1000;   // OK
      #pragma omp parallel num_threads(5)
      {
         // cannot assign to 'x' here
         x = omp_get_thread_num() + 1000;   // C3899
         System::Console::WriteLine("thread {0}", omp_get_thread_num());
      }
      x = omp_get_thread_num() + 1000;   // OK
   }
};

int main() {
   R^ r = gcnew R;
   System::Console::WriteLine(r->x);
}
```