---
title: 컴파일러 오류 C3859
ms.date: 11/04/2016
f1_keywords:
- C3859
helpviewer_keywords:
- C3859
ms.assetid: 40e93b25-4393-4467-90de-035434a665c7
ms.openlocfilehash: be6ccaab49cb329e862fb6068af1337eddbaac8f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50490281"
---
# <a name="compiler-error-c3859"></a>컴파일러 오류 C3859

PCH에 대한 가상 메모리 범위를 초과했습니다. 명령줄 옵션을 '-Zmvalue' 이상으로 지정하여 다시 컴파일하세요.

미리 컴파일된 헤더가 컴파일러에서 넣으려는 데이터의 양에 비해 너무 작습니다. 사용 된 **/Zm** 컴파일러 플래그를 미리 컴파일된 헤더 파일에 대 한 더 큰 값을 지정 합니다. 자세한 내용은 [/Zm (지정 미리 컴파일된 헤더 메모리 할당 제한)](../../build/reference/zm-specify-precompiled-header-memory-allocation-limit.md)합니다.