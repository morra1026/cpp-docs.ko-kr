---
title: --작업 주석 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- Operations comment in MFC source files
- comments, MFC
- MFC source files, Operations comments
ms.assetid: f3bff48d-26be-4db6-8435-9e4d079838c9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 73c4a7a70c9f2ed987337426793bd462c2a94309
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46372498"
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

