---
title: 빠른 컴파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- performance, cle.exe compiler
- compilation, performance
- cl.exe compiler, performance
- fast compiling
ms.assetid: 5fead136-ba69-40c8-8e25-236f89d5990a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 926c63d3d556d1aa9b85a7ce97e93b60e7c2ea23
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45722270"
---
# <a name="fast-compilation"></a>컴파일 속도 향상

컴파일 속도 늘리려면:

- 사용 하 여 [최소 다시 빌드](../../build/reference/gm-enable-minimal-rebuild.md)에 c + + 컴파일러 다시 컴파일하는 소스 파일을 클래스 헤더 파일에 변경 내용에 종속 된 경우에 합니다.

- [미리 컴파일된 헤더 파일을 만듭니다](../../build/reference/creating-precompiled-header-files.md) 하 고 사용 합니다 [헤더 옵션을 미리 컴파일된](../../build/reference/yc-create-precompiled-header-file.md)합니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)