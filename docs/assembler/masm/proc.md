---
title: PROC | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- PROC
dev_langs:
- C++
helpviewer_keywords:
- PROC directive
ms.assetid: ee5bb6b6-fa15-4d73-b0cf-e650178539a9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3ee26e181f0f40126c86a36889c43405f0b40f5e
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43680848"
---
# <a name="proc"></a>PROC

호출 프로시저 블록의 시작 및 끝 표시 *레이블*합니다. 블록의 문에서 호출할 수는 **호출** 명령 또는 [INVOKE](../../assembler/masm/invoke.md) 지시문입니다.

## <a name="syntax"></a>구문

> *레이블을* PROC [[*거리*]] [[*langtype*]] [[*가시성*]] [[\<*prologuearg*>]] [[ 사용 하 여 *reglist*]] [[합니다 *매개 변수* [[:*태그*]]]...<br/>
> [[프레임 [[:*ehandler 주소*]]]]<br/>
> *문*<br/>
> *레이블* ENDP

## <a name="remarks"></a>설명

[[프레임 [[:*ehandler 주소*]]]] ml64.exe를 사용 하 여만 유효 하 고 MASM.pdata 함수 테이블 항목을 생성 하 여 함수의 구조적에 대 한.xdata에서 정보를 해제 하면 예외 처리 동작을 해제 합니다.

경우는 **프레임** 특성을 사용 하 여 따라야는 [합니다. 프롤로그 끝](../../assembler/masm/dot-endprolog.md) 지시문입니다.

참조 [MASM (ml64.exe) x64](../../assembler/masm/masm-for-x64-ml64-exe.md) ml64.exe를 사용 하 여 대 한 자세한 내용은 합니다.

## <a name="example"></a>예제

```asm
; ml64 ex1.asm /link /entry:Example1 /SUBSYSTEM:CONSOLE
_text SEGMENT
Example1 PROC FRAME
   push r10
.pushreg r10
   push r15
.pushreg r15
   push rbx
.pushreg rbx
   push rsi
.pushreg rsi
.endprolog
   ; rest of function ...
   ret
Example1 ENDP
_text ENDS
END
```

위의 코드는 다음 함수 테이블 내보내고 정보를 해제 됩니다.

```Output
FileHeader->Machine 34404
Dumping Unwind Information for file ex2.exe

.pdata entry 1 0x00001000 0x00001023

  Unwind data: 0x00002000

    Unwind version: 1
    Unwind Flags: None
    Size of prologue: 0x08
    Count of codes: 3
    Frame register: rbp
    Frame offset: 0x0
    Unwind codes:

      Code offset: 0x08, SET_FPREG, register=rbp, offset=0x00
      Code offset: 0x05, ALLOC_SMALL, size=0x10
      Code offset: 0x01, PUSH_NONVOL, register=rbp
```

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>