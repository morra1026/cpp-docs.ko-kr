---
title: 스택 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 383f0072-0438-489f-8829-cca89582408c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 827a129c0b7a444cc5b48ba68a3e360712e1c08e
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45721541"
---
# <a name="stack-usage"></a>스택 사용

RSP의 현재 주소를 넘는 모든 메모리 일시적인 것으로 간주 됩니다: OS, 또는 디버거 사용자 디버그 세션 또는 인터럽트 처리기 중이 메모리를 덮어쓸 수 있습니다. 따라서 RSP 항상 읽기 또는 스택 프레임으로 값을 쓰기를 시도 하기 전에 설정 해야 합니다.

이 섹션에서는 로컬 변수에 대 한 스택 공간이 할당에 설명 하며 **alloca** 내장 함수입니다.

- [스택 할당](../build/stack-allocation.md)

- [동적 매개 변수 스택 영역 생성](../build/dynamic-parameter-stack-area-construction.md)

- [함수 형식](../build/function-types.md)

- [malloc 맞춤](../build/malloc-alignment.md)

- [alloca](../build/alloca.md)

## <a name="see-also"></a>참고 항목

[x64 소프트웨어 규칙](../build/x64-software-conventions.md)