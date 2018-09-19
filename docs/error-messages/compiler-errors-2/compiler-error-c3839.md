---
title: 컴파일러 오류 C3839 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3839
dev_langs:
- C++
helpviewer_keywords:
- C3839
ms.assetid: 0957faff-1e9f-439b-876b-85bd8d2c578d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 597d02ff347d399833e2376743b50f65e7674a18
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46092910"
---
# <a name="compiler-error-c3839"></a>컴파일러 오류 C3839

관리되는 또는 WinRT 형식의 맞춤 방식을 변경할 수 없습니다.

변수의 맞춤 관리 또는 Windows 런타임 형식 CLR 또는 Windows 런타임에서 제어 되며 수정할 수 없습니다 [맞춤](../../cpp/align-cpp.md)합니다.

다음 샘플에서는 C3839를 생성합니다.

```
// C3839a.cpp
// compile with: /clr
ref class C
{
public:
   __declspec(align(32)) int m_j; // C3839
};

int main()
{
}
```