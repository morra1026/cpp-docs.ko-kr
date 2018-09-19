---
title: NMAKE 심각한 오류 U1051 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1051
dev_langs:
- C++
helpviewer_keywords:
- U1051
ms.assetid: fede5cd5-dac3-47b7-b86d-e1acfb78699f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d3d3a14b75a30aa22bcc9faafb97a218051bb080
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045018"
---
# <a name="nmake-fatal-error-u1051"></a>NMAKE 심각한 오류 U1051

메모리가 부족 합니다.

NMAKE는 메이크파일 너무 크거나 복잡 한 되었으므로 가상 메모리를 포함 하 여 메모리가 부족 합니다.

### <a name="to-fix-by-using-the-following-possible-solutions"></a>아래의 해결 방법 따라 수정합니다.

1. 디스크 공간을 확보 합니다.

1. Windows NT 페이징 파일이 나 Windows 스왑 파일의 크기를 늘립니다.

1. 메이크파일의 일부만 사용 중인 경우 메이크파일 별도 파일로 분할 하거나 사용 하 여 **! IF** 전처리 지시문 NMAKE 처리 해야 하는 크기를 제한 합니다. **! IF** 지시문에는 **! IF**하십시오 `!IFDEF`, **! IFNDEF**, **! ELSE IF**, **! ELSE** `IFDEF`, 및 **! ELSE** `IFNDEF`합니다.