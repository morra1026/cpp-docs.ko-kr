---
title: 지연 로드된 가져오기 덤프
ms.date: 11/04/2016
helpviewer_keywords:
- delay-loaded imports, dumping
- imports (delay-loaded)
- delay-loaded imports
ms.assetid: f766acf4-9df8-4b85-8cf6-0be3ffc4c124
ms.openlocfilehash: 782da0d29024a8308de0bb4d00656b850629c8ba
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50444163"
---
# <a name="dumping-delay-loaded-imports"></a>지연 로드된 가져오기 덤프

지연 로드된 가져오기는 [/imports dumpbin](../../build/reference/imports-dumpbin.md)를 사용하여 덤프될 수 있으며 표준 가져오기와 약간 다른 내용을 표시합니다. 이러한 덤프 /imports 고유한 섹션으로 분리 되 고는 명시적으로 지연 로드 가져오기로 레이블이 지정 합니다. 가 언로드 정보가 이미지에는 표시 됩니다. 바인드 정보가 있으면 대상 DLL의 날짜/시간 스탬프 가져오기 바인딩된 주소와 함께 표시 됩니다.

## <a name="see-also"></a>참고 항목

[링커의 지연 로드된 DLL 지원](../../build/reference/linker-support-for-delay-loaded-dlls.md)