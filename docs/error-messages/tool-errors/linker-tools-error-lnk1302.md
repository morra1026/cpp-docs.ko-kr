---
title: 링커 도구 오류 LNK1302
ms.date: 11/04/2016
f1_keywords:
- LNK1302
helpviewer_keywords:
- LNK1302
ms.assetid: aea3c753-c2c4-4249-bbc3-f2d4f0164b5e
ms.openlocfilehash: c3b1117b31db4759b385943323a581da7a58f0c4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50491080"
---
# <a name="linker-tools-error-lnk1302"></a>링커 도구 오류 LNK1302

안전한 .netmodules 링크만 지원됩니다. .netmodule 파일을 링크할 수 없습니다.

.Netmodule (사용 하 여 컴파일된 **/LN**) MSIL 링크를 호출 하려는 사용자 시도가 링커로 전달 되었습니다.  C + + 모듈을 사용 하 여 컴파일된 MSIL 링크에 대 한 유효 **/clr: safe**합니다.

사용 하 여 컴파일하면이 오류를 해결 하려면 **/clr: safe** MSIL 링크를 사용 하도록 설정 하거나 전달 하는 **/clr** 또는 **/clr: pure** 모듈 대신 링커에.obj 파일.

자세한 내용은 다음 항목을 참조하세요.

- [/LN(MSIL 모듈 만들기)](../../build/reference/ln-create-msil-module.md)

- [링커 입력 파일로 사용하는 .netmodule 파일](../../build/reference/netmodule-files-as-linker-input.md)