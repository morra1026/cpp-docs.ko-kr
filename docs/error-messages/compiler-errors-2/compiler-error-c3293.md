---
title: 컴파일러 오류 C3293
ms.date: 07/21/2017
f1_keywords:
- C3293
helpviewer_keywords:
- C3293
ms.assetid: b772cf98-52e0-4e24-be23-1f5d87d999ac
ms.openlocfilehash: 84d539722474d5f5dfffe1f6fe121bb7349ba131
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50548212"
---
# <a name="compiler-error-c3293"></a>컴파일러 오류 C3293

'accessor': 'default'를 사용하여 'type' 클래스의 기본 속성(인덱서)에 액세스하세요.

인덱싱된 속성에 잘못 액세스했습니다.  참조 [방법: 사용 하 여 속성 C + + CLI](../../dotnet/how-to-use-properties-in-cpp-cli.md) 자세한 내용은 합니다.

**Visual Studio 2017 이상**: Visual Studio 2015 및 이전 버전에서는 일부 경우에 컴파일러는 기본 속성을 기본 인덱서로 misidentified 합니다. 속성에 액세스하는 데 식별자 "default"를 사용하여 문제를 해결할 수 있었습니다. default가 C++11에서 키워드로 도입된 이후 해결 방법 자체가 문제가 되었습니다. 따라서 Visual Studio 2017에서는 해결 방법이 필요했던 버그가 수정되었고 이제 컴파일러는 "default"가 클래스에 대한 기본 속성에 액세스하는 데 사용될 경우 오류를 발생시킵니다.

## <a name="example"></a>예제

다음 샘플에서는 C3293 Visual Studio 2015 및 이전 버전을 생성 합니다.

```
// C3293.cpp
// compile with: /clr /c
using namespace System;
ref class IndexerClass {
public:
   // default indexer
   property int default[int] {
      int get(int index) { return 0; }
      void set(int index, int value) {}
   }
};

int main() {
   IndexerClass ^ ic = gcnew IndexerClass;
   ic->Item[0] = 21;   // C3293 in VS2015 OK in VS2017
   ic->default[0] = 21;   // OK in VS2015 and earlier

   String ^s = "Hello";
   wchar_t wc = s->Chars[0];   // C3293 in VS2015 OK in VS2017
   wchar_t wc2 = s->default[0];   // OK in VS2015 and earlier
   Console::WriteLine(wc2);
}
```