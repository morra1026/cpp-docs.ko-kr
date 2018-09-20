---
title: 포함 파일에 대 한 다중 스레딩 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- threading [C++], include files
- include files, multithreading
- multithreading [C++], include files
ms.assetid: 98d764f9-71f4-4da5-8f3a-8d2d26e96799
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 64ba6ec639151ca659e3bd075f691176ef4edbdd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46422326"
---
# <a name="include-files-for-multithreading"></a>다중 스레딩을 위한 포함 파일

파일을 포함 하는 표준 라이브러리에서 구현 된 대로 C 런타임 라이브러리 함수를 선언 합니다. 사용 하는 경우는 [전체 최적화](../build/reference/ox-full-optimization.md) (/ Ox) 또는 [fastcall 호출 규칙](../build/reference/gd-gr-gv-gz-calling-convention.md) (/ Gr) 옵션 컴파일러 레지스터 호출 규칙을 사용 하 여 모든 함수 호출 수입니다. 런타임 라이브러리 함수가 C 호출 규칙을 사용 하 여 컴파일된 및 표준 포함 파일의 선언에 이러한 함수에 대 한 올바른 외부 참조를 생성 하도록 컴파일러에 지시 합니다.

## <a name="see-also"></a>참고 항목

[C 및 Win32를 사용한 다중 스레딩](multithreading-with-c-and-win32.md)