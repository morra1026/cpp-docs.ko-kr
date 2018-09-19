---
title: 링커 도구 오류 LNK1107 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1107
dev_langs:
- C++
helpviewer_keywords:
- LNK1107
ms.assetid: a37a893d-5efa-4eba-8f40-6c5518b4b9d0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 73a1643d10ea9adc6ac6979eb2de023593ba8d01
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46060709"
---
# <a name="linker-tools-error-lnk1107"></a>링커 도구 오류 LNK1107

파일이 잘못 되었거나 손상 되었습니다: 위치에서 읽을 수 없습니다

도구 파일을 읽을 수 없습니다. 파일을 다시 만듭니다.

모듈을 전달 하면 LNK1107 발생할 수 있습니다 (.dll 또는.netmodule 확장을 사용 하 여 만든 [/clr:noAssembly](../../build/reference/clr-common-language-runtime-compilation.md) 또는 [/NOASSEMBLY](../../build/reference/noassembly-create-a-msil-module.md)) 링커에;.obj 파일에 대신 전달 합니다.

다음 샘플 컴파일하는 경우:

```
// LNK1107.cpp
// compile with: /clr /LD
public ref class MyClass {
public:
   void Test(){}
};
```

다음을 지정 **LNK1107.dll 링크** 명령줄 LNK1107 시킬 수 있습니다.  이 오류를 해결 하려면 지정 **LNK1107.obj 링크** 대신 합니다.