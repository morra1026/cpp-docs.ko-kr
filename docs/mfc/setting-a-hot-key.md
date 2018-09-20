---
title: 바로 가기 키를 설정 합니다. | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- keyboard shortcuts [MFC], hot keys
- access keys [MFC], hot keys
- CHotKeyCtrl class [MFC], setting hot key
ms.assetid: 6f3bc141-e346-4dce-9ca7-3e6b2c453f3f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0c634f9eac562be2b22f79e6a71c3010e3ea3e24
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46435237"
---
# <a name="setting-a-hot-key"></a>바로 가기 키 설정

응용 프로그램 바로 가기 키를 제공 하는 정보를 사용할 수 있습니다 ([CHotKeyCtrl](../mfc/reference/chotkeyctrl-class.md))의 두 가지 방법으로 제어 합니다.

- 전송 하 여 비 자식 창을 활성화 하기 위한 전역 바로 가기 키를 설정 된 [WM_SETHOTKEY](/windows/desktop/inputdev/wm-sethotkey) 활성화할 창에 메시지.

- Windows 함수를 호출 하 여 스레드 관련 바로 가기 키를 설정 [RegisterHotKey](https://msdn.microsoft.com/library/windows/desktop/ms646309)합니다.

## <a name="see-also"></a>참고 항목

[CHotKeyCtrl 사용](../mfc/using-chotkeyctrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

