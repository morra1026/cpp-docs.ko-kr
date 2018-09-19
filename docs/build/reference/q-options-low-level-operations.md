---
title: -Q 옵션 (하위 수준 작업) | Microsoft Docs
ms.custom: ''
ms.date: 1/23/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /q
dev_langs:
- C++
helpviewer_keywords:
- Q compiler option [C++]
- -Q compiler option [C++]
- /Q compiler option [C++]
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 15854333a9f26f87d20f7819327e68050ab37bf6
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45717788"
---
# <a name="q-options-low-level-operations"></a>/Q 옵션(하위 수준 작업)

사용할 수는 **/Q** 다음 하위 수준의 컴파일러 작업을 수행 하려면 컴파일러 옵션:

- [/Qfast_transcendentals (빠른 초월수 강제 적용)](../../build/reference/qfast-transcendentals-force-fast-transcendentals.md): 빠른 초월수를 생성 합니다.

- [/Qifist (_ftol 표시 안 함)](../../build/reference/qifist-suppress-ftol.md): 억제 `_ftol` 정수 형식이 부동 소수점 형식에서 변환할 때 필요한 x86 전용입니다.

- [/Qimprecise_fwaits (Try 블록 내의 fwait 제거)](../../build/reference/qimprecise-fwaits-remove-fwaits-inside-try-blocks.md): 제거 `fwait` 내에서 명령을 `try` 블록입니다.

- [/Qpar (자동 평행 화 도우미)](../../build/reference/qpar-auto-parallelizer.md): 사용 하 여 표시 되는 루프의 자동 병렬화 할 수 있도록 합니다 [#pragma loop ()](../../preprocessor/loop.md) 지시문입니다.

- [/Qpar-report (자동 평행 화 도우미 보고 수준)](../../build/reference/qpar-report-auto-parallelizer-reporting-level.md): 자동 병렬화에 대 한 수준을 보고 사용 하도록 설정 합니다.

- [/Qsafe_fp_loads](../../build/reference/qsafe-fp-loads.md): 부동 소수점 레지스터 로드 하 고 메모리 및 MMX 간 이동에 대 한 등록에 대 한 최적화가 억제 됩니다.

- [/Qspectre](../../build/reference/qspectre.md): 특정 스펙터 보안 취약성을 완화 하는 명령을 생성 합니다.

- [/Qvec-report (자동 벡터화 도우미 보고 수준)](../../build/reference/qvec-report-auto-vectorizer-reporting-level.md): 자동 벡터화에 대 한 수준을 보고 사용 하도록 설정 합니다.

## <a name="see-also"></a>참고자료

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)
