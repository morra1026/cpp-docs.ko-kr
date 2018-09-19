---
title: 연결 된 해제 정보 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 176835bf-f118-45d9-9128-9db4b7571864
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6da09387595188026d855fb99a49b588e6f21aa3
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45715028"
---
# <a name="chained-unwind-info-structures"></a>연결된 해제 정보 구조체

UNW_FLAG_CHAININFO 플래그가 설정 된 경우에 해제 정보 구조체는 보조 단일 되 고 기본 해제 정보를 포함 하는 공유 되는 예외 처리기/연결-정보 주소 필드 다음 코드 검색 주 해제 라고 가정할 때 내용은 `unwindInfo` 구조는 UNW_FLAG_CHAININFO 있는 플래그가 설정 됩니다.

```
PRUNTIME_FUNCTION primaryUwindInfo = (PRUNTIME_FUNCTION)&(unwindInfo->UnwindCode[( unwindInfo->CountOfCodes + 1 ) & ~1]);
```

연결 된 정보는 두 가지 상황에서 유용 합니다. 첫째, 불연속 코드 세그먼트에 사용할 수 있습니다. 연결 된 정보를 사용 하 여 기본 해제 정보에서 해제 코드 배열은 중복 없기 때문에 필요한 해제 정보의 크기를 줄일 수 있습니다.

또한 휘발성 레지스터 저장을 그룹에 연결 된 정보를 사용할 수 있습니다. 컴파일러는 함수 진입점 프롤로그 외부에서 될 때까지 일부 휘발성 레지스터 저장 지연 될 수 있습니다. 그룹화 된 코드가 전에 함수 부분에 대 한 정보를 주 해제 함으로써이 기록할 수 있습니다 하 고 프롤로그에 있는 연결 된 정보는 해제 코드 비휘발성 레지스터의 0이 아닌 크기를 사용 하는 정보를 연결로 설정 합니다. 이 경우 해제 코드는 UWOP_SAVE_NONVOL의 모든 인스턴스입니다. 푸시를 사용 하 여 비휘발성 레지스터를 저장 하거나 추가 고정된 스택 할당을 사용 하 여 RSP 레지스터를 수정 하는 그룹화가 지원 되지 않습니다.

설정 UNW_FLAG_CHAININFO 있는 UNWIND_INFO 항목 UNWIND_INFO 항목이 있습니다 (여러 래핑) 설정 UNW_FLAG_CHAININFO RUNTIME_FUNCTION 항목을 포함할 수 있습니다. 결과적으로 연결 된 해제 포인터 삭제; UNW_FLAG_CHAININFO 있는 UNWIND_INFO 항목에 도착 하는 정보 이것이 실제 프로시저 진입점을 가리키는 주 UNWIND_INFO 항목입니다.

## <a name="see-also"></a>참고 항목

[디버거 지원, 예외 처리를 위한 해제 데이터](../build/unwind-data-for-exception-handling-debugger-support.md)