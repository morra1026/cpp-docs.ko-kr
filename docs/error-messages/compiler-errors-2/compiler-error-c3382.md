---
title: 컴파일러 오류 C3382
ms.date: 11/04/2016
f1_keywords:
- C3382
helpviewer_keywords:
- C3382
ms.assetid: a7603abd-ac4e-4ae6-a02b-3bdc6d1908a6
ms.openlocfilehash: c262ea963ae739fbb76211aae2622e98d5a9b6f7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50462753"
---
# <a name="compiler-error-c3382"></a>컴파일러 오류 C3382

/clr:safe를 지정하면 'sizeof'를 사용할 수 없습니다.

**/clr:safe** 컴파일의 출력 파일은 형식 안전 파일이며 sizeof는 지원되지 않습니다. sizeof 연산자의 반환 값은 size_t이며 운영 체제에 따라 크기가 달라지기 때문입니다.

자세한 내용은 다음 항목을 참조하세요.

- [sizeof 연산자](../../cpp/sizeof-operator.md)

- [/clr(공용 언어 런타임 컴파일)](../../build/reference/clr-common-language-runtime-compilation.md)

- [일반적인 Visual C++ 64비트 마이그레이션 문제](../../build/common-visual-cpp-64-bit-migration-issues.md)

## <a name="example"></a>예제

다음 샘플에서는 C3382를 생성합니다.

```
// C3382.cpp
// compile with: /clr:safe
int main() {
   sizeof( char );   // C3382
}
```