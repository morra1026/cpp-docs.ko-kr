---
title: 파일 닫기 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MFC, file operations
- files [MFC], closing
ms.assetid: 8415a3a8-3c75-45b0-ac2a-d5385f49bdb3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9c392ef728e1d796a02cfa32edc2c3e8c74d083b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46426239"
---
# <a name="closing-files"></a>파일 닫기

일반적으로 I/O 작업에서 파일을 마친 후 닫아야 합니다.

#### <a name="to-close-a-file"></a>파일을 닫으려면

1. 사용 된 **닫기** 멤버 함수입니다. 이 함수는 파일 시스템 파일을 닫고 필요한 경우 버퍼를 플러시합니다.

할당 한 경우는 [CFile](../mfc/reference/cfile-class.md) 프레임에서 개체 (에 표시 된 예제와 같이 [파일 열기](../mfc/opening-files.md)), 개체는 자동으로 닫히고 다음 범위를 벗어나면 제거 합니다. 해당 삭제를 확인 합니다 `CFile` 개체 파일 시스템에 물리적 파일을 삭제 되지 않습니다.

## <a name="see-also"></a>참고 항목

[파일](../mfc/files-in-mfc.md)

