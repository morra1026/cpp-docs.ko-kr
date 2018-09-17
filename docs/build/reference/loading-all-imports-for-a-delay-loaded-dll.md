---
title: 지연 로드 된 DLL에 대 한 모든 가져오기 로드 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- __HrLoadAllImportsForDll linker option
ms.assetid: 975fcd97-1a56-4a16-9698-e1a249d2d592
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 29ef1c576af7930e157dafd0f57bf0b8dff49fa6
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45715587"
---
# <a name="loading-all-imports-for-a-delay-loaded-dll"></a>지연 로드된 DLL에 대한 모든 가져오기 로드

합니다 **__HrLoadAllImportsForDll** delayhlp.cpp에 정의 된 함수에는 지정 된 DLL에서 모든 가져오기 로드 하도록 링커에 지시 합니다 [/delayload](../../build/reference/delayload-delay-load-import.md) 링커 옵션.

모든 가져오기 로드 기능을 사용 하면 코드에서 한 곳에서 오류 처리 및 예외 처리를 실제로 가져오기 호출할 때 사용할 필요가 없습니다. 또한 가져오기 로드에 실패 하는 도우미 코드의 결과로 프로세스를 통해 응용 프로그램을 부분적으로 실패 하는 상황을 방지 합니다.

호출 **__HrLoadAllImportsForDll** 후크 및 오류 동작을 변경 하지 않는 참조 처리; [오류 처리 및 알림](../../build/reference/error-handling-and-notification.md) 자세한 내용은 합니다.

DLL 이름에 전달 **__HrLoadAllImportsForDll** DLL 자체 내에 저장 하는 이름을 비교 되 고 대 소문자를 구분 합니다.

다음 예제에서는 호출 하는 방법을 보여 줍니다 **__HrLoadAllImportsForDll**:

```
if (FAILED(__HrLoadAllImportsForDll("delay1.dll"))) {
   printf ( "failed on snap load, exiting\n" );
   exit(2);
}
```

## <a name="see-also"></a>참고 항목

[링커의 지연 로드된 DLL 지원](../../build/reference/linker-support-for-delay-loaded-dlls.md)