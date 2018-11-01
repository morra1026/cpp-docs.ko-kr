---
title: '방법: char * 문자열을 System::Byte 배열로 변환'
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- examples [C++], strings
- arrays [C++], character
- character arrays, converting to System::Byte arrays
- examples [C++], arrays
ms.assetid: de9bc4eb-773c-4796-a496-9b90ca986503
ms.openlocfilehash: 26ef83533e7da1d272c31a54165626f513a5508a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50594729"
---
# <a name="how-to-convert-char--string-to-systembyte-array"></a>방법: char 변환 \* 문자열을 system:: byte 배열로

변환 하는 가장 효율적인 방법은 `char *` 문자열을 <xref:System.Byte> 배열을 사용 하는 것 <xref:System.Runtime.InteropServices.Marshal> 클래스입니다.

## <a name="example"></a>예제

```
// convert_native_string_to_Byte_array.cpp
// compile with: /clr
#include <string.h>

using namespace System;
using namespace System::Runtime::InteropServices;

int main() {
   char buf[] = "Native String";
   int len = strlen(buf);

   array< Byte >^ byteArray = gcnew array< Byte >(len + 2);

   // convert native pointer to System::IntPtr with C-Style cast
   Marshal::Copy((IntPtr)buf,byteArray, 0, len);

   for ( int i = byteArray->GetLowerBound(0); i <= byteArray->GetUpperBound(0); i++ ) {
      char dc =  *(Byte^)   byteArray->GetValue(i);
      Console::Write((Char)dc);
   }

   Console::WriteLine();
}
```

```Output
Native String
```

## <a name="see-also"></a>참고 항목

[C++ Interop 사용(암시적 PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)