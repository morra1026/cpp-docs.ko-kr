---
title: 컴파일러 경고 (수준 1) C4397 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4397
dev_langs:
- C++
helpviewer_keywords:
- C4397
ms.assetid: 6346fdc2-dbbf-4fba-803a-32b0d0a707be
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f5a3ccc7b55a9a4aabad5d5567f08b0a56d4ba87
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064531"
---
# <a name="compiler-warning-level-1-c4397"></a>컴파일러 경고(수준 1) C4397

DefaultCharSetAttribute가 무시 됩니다.

<xref:System.Runtime.InteropServices.DefaultCharSetAttribute> Visual c + + 컴파일러에서 무시 됩니다. DLL에 대해 설정 하는 문자를 지정 하려면 DllImport의 CharSet 옵션을 사용 합니다. 자세한 내용은 [c + + Interop 사용 (암시적 PInvoke)](../../dotnet/using-cpp-interop-implicit-pinvoke.md)합니다.

## <a name="example"></a>예제

다음 샘플 C4397를 생성합니다.

```
// C4397.cpp
// compile with: /W1 /c /clr
using namespace System;
using namespace System::Runtime::InteropServices;

[module:DefaultCharSetAttribute(CharSet::Unicode)];   // C4397

[DllImport("kernel32", EntryPoint="CloseHandle", CharSet=CharSet::Unicode)]   // OK
extern "C" bool ImportDefault(IntPtr hObject);

public ref class MySettingVC {
public:
   void method() {
      ImportDefault(IntPtr::Zero);
   }
};

[StructLayout(LayoutKind::Explicit)]
public ref struct StructDefault1{};

public ref class ClassDefault1{};
```