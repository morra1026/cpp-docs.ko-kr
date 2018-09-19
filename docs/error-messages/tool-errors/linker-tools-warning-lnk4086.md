---
title: 링커 도구 경고 LNK4086 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4086
dev_langs:
- C++
helpviewer_keywords:
- LNK4086
ms.assetid: ea1eecbb-ba2c-41bb-9a4f-fa0808a4b92d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 21a2ee7660f0ad78d04f7edb191929296c8d47a9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46079234"
---
# <a name="linker-tools-warning-lnk4086"></a>링커 도구 경고 LNK4086

entrypoint 'function' 'number' 바이트 인수가 있는 __stdcall이 아닙니다. 이미지를 실행할 수 없습니다.

Dll 진입점 이어야 `__stdcall`합니다. 사용 하 여 함수를 다시 컴파일 중 하나는 [/Gz](../../build/reference/gd-gr-gv-gz-calling-convention.md) 옵션 또는 지정 `__stdcall` 또는 WINAPI 함수를 정의 하는 경우.