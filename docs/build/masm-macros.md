---
title: MASM 매크로
ms.date: 11/04/2016
ms.assetid: 21410432-72fc-4795-bc93-e78123f9f14f
ms.openlocfilehash: 8a00852a3a763aae5fda34d7e0fde664997a0bdb
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/09/2018
ms.locfileid: "51328827"
---
# <a name="masm-macros"></a>MASM 매크로

사용을 간소화 하기 위해 합니다 [원시 의사 작업](../build/raw-pseudo-operations.md), 일반적인 프로시저 프롤로그 및 에필로그를 만드는 데 사용할 수 있습니다 ksamd64.inc에 정의 된 매크로의 집합입니다.

## <a name="remarks"></a>설명

|매크로|설명|
|-----------|-----------------|
|alloc_stack(n)|(N 하위 rsp 사용), n 바이트의 스택 프레임을 할당 하 고 내보내는 적절 한 해제 정보 (.allocstack n)|
|save_reg reg, loc|에 RSP 오프셋된 위치에 있는 스택의 비휘발성 레지스터 reg 저장 및 내보내는 적절 한 정보를 해제 합니다. (.savereg reg, loc)|
|push_reg reg|비휘발성 레지스터 reg 스택에 푸시하고 내보내는 적절 한 정보를 해제 합니다. 생성 합니다.|
|rex_push_reg reg|2 바이트 푸시를 사용 하 여 스택에 비휘발성 레지스터를 저장 하 고 내보내는 적절 한 해제 정보 생성 합니다. 푸시는 함수에서 첫 번째 명령을 핫 패치 가능한 함수 인지 확인 하는 경우 사용 해야 합니다.|
|save_xmm128 reg, loc|XMM 등록 비휘발성 reg RSP 오프셋된 loc를 스택에 저장 및 내보내는 적절 한 정보 (. savexmm128 reg, loc) 해제|
|set_frame reg 오프셋|프레임 등록 reg를 RSP 수 + (mov, 또는 사용 하는 유지) 오프셋을 설정 하 고 내보내는 적절 한 정보 (.set_frame reg, 오프셋)를 해제|
|push_eflags|Pushfq 지침을 사용 하 여 eflags 푸시하고 내보내는 적절 한 해제 정보 (.alloc_stack 8)|

적절 한 매크로 사용 하 여 샘플 함수 프롤로그는 다음과 같습니다.

```asm
SkFrame struct
Fill    dq ?; fill to 8 mod 16
SavedRdi dq ?; saved register RDI
SavedRsi dq ?; saved register RSI
SkFrame ends

sampleFrame struct
Filldq?; fill to 8 mod 16
SavedRdidq?; Saved Register RDI
SavedRsi  dq?; Saved Register RSI
sampleFrame ends

sample2 PROC FRAME
alloc_stack(sizeof sampleFrame)
save_reg rdi, sampleFrame.SavedRdi
save_reg rsi, sampleFrame.SavedRsi
.end_prolog

; function body

    mov rsi, sampleFrame.SavedRsi[rsp]
    mov rdi, sampleFrame.SavedRdi[rsp]

; Here’s the official epilog

    add rsp, (sizeof sampleFrame)
    ret
sample2 ENDP
```

## <a name="see-also"></a>참고 항목

[MASM에 대한 해제 도우미](../build/unwind-helpers-for-masm.md)