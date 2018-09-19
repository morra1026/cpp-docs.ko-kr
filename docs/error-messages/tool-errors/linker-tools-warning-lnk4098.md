---
title: 링커 도구 경고 LNK4098 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4098
dev_langs:
- C++
helpviewer_keywords:
- LNK4098
ms.assetid: 1f1b1408-1316-4e34-80f5-6a02f2db0ac1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2068534d51ae1350510a349f875c1977299edb1d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46019156"
---
# <a name="linker-tools-warning-lnk4098"></a>링커 도구 경고 LNK4098

다른 라이브러리;의 사용과 defaultlib 'library' 충돌 사용 합니다

호환 되지 않는 라이브러리를 사용 하 여 연결 하려고 합니다.

> [!NOTE]
>  이제 런타임 라이브러리 여러 형식이 혼합을 방지 하기 위해 지시문 포함 됩니다. 동일한 프로그램에서이 다른 형식을 사용 하거나 디버그 하려고 하면 경고 및 런타임 라이브러리의 디버그 버전 받습니다. 예를 들어 다른 종류를 사용 하 여 (예: 다중 스레드 및 단일 스레드)에 파일을 연결 하려고 했습니다. 종류의 런타임 라이브러리 및 다른 하나를 사용 하려면 파일을 컴파일한 경우이 경고를 받습니다. 모든 소스 파일을 동일한 런타임 라이브러리를 사용 하 여 컴파일해야 합니다. 참조를 [런타임 라이브러리 사용](../../build/reference/md-mt-ld-use-run-time-library.md) (**/MD**에 **/MT**를 **/LD**) 컴파일러 옵션을 참조 하십시오.

링커의 사용할 수 있습니다 [/verbose: lib](../../build/reference/verbose-print-progress-messages.md) 스위치 링커가 검색 하는 라이브러리를 확인할 수 있습니다. 비-디버그 런타임 라이브러리를 사용 하 여 LNK4098을 사용 하는 예는 단일 스레드 실행 파일을 만들려는 경우 합니다 **/verbose: lib** 라이브러리는 링커가 검색 하는 옵션입니다. 링커는 검색 라이브러리로 LIBC.lib 및 LIBCMT.lib, MSVCRT.lib, LIBCD.lib, LIBCMTD.lib, 않거나 MSVCRTD.lib를 인쇄 해야 합니다. 사용 하 여 잘못 된 런타임 라이브러리를 무시 하도록 링커에 지시할 수 있습니다 [/NODEFAULTLIB](../../build/reference/nodefaultlib-ignore-libraries.md) 무시 하려는 각 라이브러리에 대 한 합니다.

다음 표에서 런타임 라이브러리에 따라 사용 하려는 라이브러리를 무시 합니다.

|이 런타임 라이브러리 사용|이러한 라이브러리를 무시 합니다.|
|-----------------------------------|----------------------------|
|단일 스레드 (libc.lib)|libcmt.lib, msvcrt.lib, libcd.lib, libcmtd.lib, msvcrtd.lib|
|다중 스레드 (libcmt.lib)|libc.lib, msvcrt.lib, libcd.lib, libcmtd.lib, msvcrtd.lib|
|다중 스레드 DLL (msvcrt.lib)를 사용 하 여|libc.lib, libcmt.lib, libcd.lib, libcmtd.lib, msvcrtd.lib|
|단일 스레드 (libcd.lib) 디버그|libc.lib, libcmt.lib, msvcrt.lib, libcmtd.lib, msvcrtd.lib|
|다중 스레드 디버그 (libcmtd.lib)|libc.lib, libcmt.lib, msvcrt.lib, libcd.lib, msvcrtd.lib|
|다중 스레드 DLL (msvcrtd.lib)를 사용 하 여 디버그|libc.lib, libcmt.lib, msvcrt.lib, libcd.lib, libcmtd.lib|

예를 들어,이 경고를 받게 디버그가 아닌, 단일 스레드 버전의 런타임 라이브러리를 사용 하는 실행 파일을 만들려는 경우 링커를 사용 하 여 다음 옵션을 사용할 수 있습니다.

```
/NODEFAULTLIB:libcmt.lib /NODEFAULTLIB:msvcrt.lib /NODEFAULTLIB:libcd.lib /NODEFAULTLIB:libcmtd.lib /NODEFAULTLIB:msvcrtd.lib
```