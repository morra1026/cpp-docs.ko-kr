---
title: 컴파일러 오류 C3505 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3505
dev_langs:
- C++
helpviewer_keywords:
- C3505
ms.assetid: ed73c99e-93a1-4f3a-bac7-ba7ed5d836e4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0d6af1b96f23332b5eed82fab2c24c93e2d53dee
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46054976"
---
# <a name="compiler-error-c3505"></a>컴파일러 오류 C3505

> 형식 라이브러리를 로드할 수 없습니다. '*guid*'

C3505는 32 비트, x86에 호스트 된 크로스 컴파일러 64 비트를 실행 하는 경우 발생할 수 있습니다, 그리고 32 비트 레지스트리 하이브에에서 읽을 x64 대상에는 64 비트 컴파일러는 WOW64에서 실행 되기 때문에 컴퓨터 및 수 있습니다.

가져오려고 하는 형식 라이브러리의 32 비트 및 64 비트 버전을 작성 하 여이 오류를 해결 하 고 둘 다 등록할 수 있습니다.  변경 해야 하는 네이티브 64 비트 컴파일러를 사용할 수 있습니다 하 **VC + + 디렉터리** 64 비트 컴파일러를 가리키도록 IDE의 속성입니다.

자세한 내용은 다음 항목을 참조하세요.

- [방법: 명령줄에서 64비트 Visual C++ 도구 집합 사용](../../build/how-to-enable-a-64-bit-visual-cpp-toolset-on-the-command-line.md)

- [방법: 64비트, x64 플랫폼을 대상으로 한 Visual C++ 프로젝트 구성](../../build/how-to-configure-visual-cpp-projects-to-target-64-bit-platforms.md)