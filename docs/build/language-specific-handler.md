---
title: 언어별 처리기 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 6503e0cd-2d3a-4330-a925-8bed8c27c2be
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 678f5695523751ebc1ef3c5dba2b63154b21833c
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45714950"
---
# <a name="language-specific-handler"></a>언어별 처리기

언어별 처리기의 상대 주소에에서 있으면는 UNWIND_INFO 때마다 UNW_FLAG_EHANDLER 또는 UNW_FLAG_UHANDLER 플래그를 설정 합니다. 이전 섹션에서 설명한 대로, 언어별 처리기는 예외 처리기 검색의 일부로 또는 해제의 일부로 호출 됩니다. 프로토타입은 다음과 같습니다.

```
typedef EXCEPTION_DISPOSITION (*PEXCEPTION_ROUTINE) (
    IN PEXCEPTION_RECORD ExceptionRecord,
    IN ULONG64 EstablisherFrame,
    IN OUT PCONTEXT ContextRecord,
    IN OUT PDISPATCHER_CONTEXT DispatcherContext
);
```

**ExceptionRecord** 표준 Win64 정의는 예외 레코드에 대 한 포인터를 제공 합니다.

**EstablisherFrame** 의이 함수에 대 한 고정된 스택 할당의 기본 주소입니다.

**ContextRecord** 예외 컨텍스트 (에서 예외 처리기) 예외가 발생 하는 경우 또는 현재 가리키는 "해제" 컨텍스트 (종료 처리기의 경우).

**DispatcherContext** 이 함수에 대 한 디스패처 컨텍스트를 가리킵니다. 다음과 같은 정의가 있습니다.

```
typedef struct _DISPATCHER_CONTEXT {
    ULONG64 ControlPc;
    ULONG64 ImageBase;
    PRUNTIME_FUNCTION FunctionEntry;
    ULONG64 EstablisherFrame;
    ULONG64 TargetIp;
    PCONTEXT ContextRecord;
    PEXCEPTION_ROUTINE LanguageHandler;
    PVOID HandlerData;
} DISPATCHER_CONTEXT, *PDISPATCHER_CONTEXT;
```

**ControlPc** 이 함수 내에서 RIP의 값입니다. 이것이 예외 주소 또는 주소는 컨트롤 왼쪽 설정 함수입니다. 이이 함수 내에서 보호 된 일부 구문 내 컨트롤 인지 확인 하는 데 사용할 RIP (에 대 한 예를 들어 __try 블록 \__try /\__except 또는 \__try /\__finally).

**ImageBase** 이미지 기본 (로드 주소)이이 함수를 함수 항목에서 사용 되는 32 비트 오프셋에 추가 되 고 해제 상대 주소를 기록 하는 정보를 포함 하는 모듈입니다.

**FunctionEntry** 는 RUNTIME_FUNCTION에 대 한 포인터를 제공 함수 진입 함수를 보유 하 고이 함수에 대 한 정보 이미지 기반 상대 주소를 해제 합니다.

**EstablisherFrame** 의이 함수에 대 한 고정된 스택 할당의 기본 주소입니다.

**TargetIp** 해제의 연속 주소를 지정 하는 선택적 명령 주소를 제공 합니다. 이 주소는 무시 됩니다 **EstablisherFrame** 지정 하지 않으면.

**ContextRecord** 시스템 예외 디스패치/해제 코드 사용에 대 한 예외 컨텍스트를 가리킵니다.

**LanguageHandler** 호출할 언어별 언어 처리기 루틴을 가리킵니다.

**HandlerData** 이 함수에 대 한 언어별 처리기 데이터를 가리킵니다.

## <a name="see-also"></a>참고 항목

[예외 처리(x64)](../build/exception-handling-x64.md)