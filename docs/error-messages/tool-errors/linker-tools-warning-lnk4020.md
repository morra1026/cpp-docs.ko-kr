---
title: 링커 도구 경고 LNK4020
ms.date: 05/29/2018
f1_keywords:
- LNK4020
helpviewer_keywords:
- LNK4020
ms.openlocfilehash: 7810fd9a97a8f6e22ad362819a024358a9f4b07c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50609744"
---
# <a name="linker-tools-warning-lnk4020"></a>링커 도구 경고 LNK4020

> 형식 레코드가 '*filename*' 손상 되었습니다; 일부 기호와 형식 디버거에서 액세스할 수 있습니다

PDB 파일 *filename* 손상 된 형식 레코드를 포함 합니다.

이 문제는 주로 기타 빌드 문제; 보조 기타 오류 및 경고를 사용 하 여 처리 하는 첫 번째 보고 된 빌드 문제를 하지 않은 경우 첫 번째입니다. 첫 번째 보고 된 문제 이면 빌드 디렉터리를 정리 하 고 프로젝트를 다시 작성 해야 합니다. 병렬 빌드 프로세스를 사용 하는 경우 빌드를 serialize 할 때 오류가 지속 되 면 참조 하세요.