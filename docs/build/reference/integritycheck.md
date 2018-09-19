---
title: /INTEGRITYCHECK | Microsoft Docs
ms.custom: ''
ms.date: 12/28/2017
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /INTEGRITYCHECK
dev_langs:
- C++
helpviewer_keywords:
- -INTEGRITYCHECK editbin options
- /INTEGRITYCHECK editbin options
- INTEGRITYCHECK editbin options
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 062ce019fe1b622661be880d8a06eac9c5971103
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45709205"
---
# <a name="integritycheck"></a>/INTEGRITYCHECK

로드 시 이진 이미지의 디지털 서명을 확인 해야 합니다는 나타냅니다.

> **/INTEGRITYCHECK**[**: NO**]

## <a name="remarks"></a>설명

DLL 파일 또는 실행 파일의 헤더에서이 옵션은 메모리 관리자에서 Windows 이미지를 로드 하려면 디지털 서명 확인을 수행 해야 하는 플래그를 설정 합니다. Windows Vista 이전의 Windows 버전은이 플래그를 무시 합니다. 이 옵션은 커널 모드 코드를 구현 하 고 모든 장치 드라이버에 대 한 권장 되는 64 비트 Dll에 대해 설정 되어야 합니다. 자세한 내용은 [커널 모드 코드 서명 요구 사항을](/windows-hardware/drivers/install/kernel-mode-code-signing-requirements--windows-vista-and-later-)합니다.

## <a name="see-also"></a>참고자료

[EDITBIN 옵션](../../build/reference/editbin-options.md)
