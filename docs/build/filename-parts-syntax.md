---
title: 파일 이름 부분 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- syntax, filename-parts
- filename-parts syntax in NMAKE
- NMAKE program, syntax
ms.assetid: 48fe38e0-3f3b-40e6-894c-330ee775a656
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5bf7a9685face739059c4b947a5796cc0a28950a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703172"
---
# <a name="filename-parts-syntax"></a>파일 이름 부분 구문

명령에서 파일 이름 부분 구문 (묵시적된는 종속 될 수 있음)는 첫 번째 종속 파일의 구성 요소를 나타냅니다. 파일 이름 구성 요소 이며 파일의 드라이브, 경로, 기본 이름 및 지정 된 대로 확장 디스크에서 아니라 사용 하 여 **%s** 전체 파일 이름을 나타내는입니다. 사용 하 여 **%&#124;**[*파트*]**F** (세로 막대 백분율 기호 뒤에 문자가), 파일 이름 부분을 나타내는 위치 *파트*순서에 관계 없이 다음 문자의 0 개 이상의 될 수 있습니다.

|글자|설명|
|------------|-----------------|
|문자 없음|전체 이름 (동일 **%s**)|
|**d**|드라이브|
|**p**|Path|
|**f**|파일 기본 이름|
|**e**|파일 확장명|

예를 들어, 파일 이름 c:\prog.exe 경우:

- %s c:\prog.exe 수는

- %&#124;F c:\prog.exe 됩니다

- %&#124;dF c 됩니다

- %&#124;pF c:\ 됩니다

- %&#124;fF prog 됩니다

- %&#124;eF exe 됩니다

## <a name="see-also"></a>참고 항목

[메이크파일의 명령](../build/commands-in-a-makefile.md)