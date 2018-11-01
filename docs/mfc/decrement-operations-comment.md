---
title: --작업 주석
ms.date: 11/04/2016
helpviewer_keywords:
- Operations comment in MFC source files
- comments, MFC
- MFC source files, Operations comments
ms.assetid: f3bff48d-26be-4db6-8435-9e4d079838c9
ms.openlocfilehash: 6b84da721bd22723d0eb5a0b520462cd8a4613e8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50653197"
---
# <a name="-operations-comment"></a>// 작업 주석

`// Operations` MFC 클래스 선언 섹션에 작업을 수행 하거나 (작업을 수행 합니다.) 작업을 수행할 수 있도록 하려면 개체에서 호출할 수 있는 멤버 함수가 포함 되어 있습니다. 이러한 함수는 일반적으로 비-**const** 부작용을 일반적으로 있기 때문에 있습니다. 가상 또는 클래스의 요구에 따라 비가상 될 수 있습니다. 일반적으로 이러한 멤버는 public입니다.

클래스에서 나열 하는 예제의 `CStdioFile`의 [주석의 예제](../mfc/an-example-of-the-comments.md),이 주석은 아래의 두 멤버 함수 목록에 포함 됩니다: `ReadString` 및 `WriteString`합니다.

특성과 마찬가지로 운영 나누어질 수 있습니다.

## <a name="see-also"></a>참고 항목

[MFC 소스 파일 사용](../mfc/using-the-mfc-source-files.md)<br/>
[주석 예](../mfc/an-example-of-the-comments.md)<br/>
[구현 주석](../mfc/decrement-implementation-comment.md)<br/>
[생성자 주석](../mfc/decrement-constructors-comment.md)<br/>
[특성 주석](../mfc/decrement-attributes-comment.md)<br/>
[재정의 가능 주석](../mfc/decrement-overridables-comment.md)

