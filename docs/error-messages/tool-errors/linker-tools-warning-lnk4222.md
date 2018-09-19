---
title: 링커 도구 경고 LNK4222 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4222
dev_langs:
- C++
helpviewer_keywords:
- LNK4222
ms.assetid: b7bb1794-41fb-4c83-b9b0-59c0d786a7da
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: abc4f85fbc361b37d9325f9d395a1c34e1eeed2e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46106938"
---
# <a name="linker-tools-warning-lnk4222"></a>링커 도구 경고 LNK4222

내보낸된 symbol '기호를 서 수로 지정 해야

다음 기호를 서 수로 내보내지 않아야 합니다.

- `DllCanUnloadNow`

- `DllGetClassObject`

- `DllGetClassFactoryFromClassString`

- `DllInstall`

- `DllRegisterServer`

- `DllRegisterServerEx`

- `DllUnregisterServer`

이름별로 항상 있는 이러한 함수를 사용 하 여 `GetProcAddress`입니다. 링커는이 경고 유형의 내보내기는 더 큰 이미지에서를 생성할 수 있으므로 합니다. 이 범위에 서 수 내보내기 비교적 적은 내보내기로 큰 경우에 발생할 수 있습니다. 예를 들어 개체에 적용된

```
EXPORTS
   DllGetClassObject   @1
   MyOtherAPI      @100
```

100 슬롯 중 98 사용 하 여 내보내기 주소 테이블에서 위의 (2-99) 해야 합니다. 다른 한편으로는

```
EXPORTS
   DllGetClassObject
   MyOtherAPI      @100
```

두 슬롯을 지정 해야 합니다. (사용 하 여 내보낼 수 있음을 알고 있어야 합니다 [/내보내기](../../build/reference/export-exports-a-function.md) 링커 옵션.)