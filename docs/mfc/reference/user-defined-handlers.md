---
title: 사용자 정의 처리기
ms.date: 11/04/2016
f1_keywords:
- vc.mfc.handlers
helpviewer_keywords:
- ON_REGISTERED_MESSAGE macro [MFC]
- ON_MESSAGE macro [MFC]
- user-defined handlers [MFC]
ms.assetid: 99478294-bef0-4ba7-a369-25a6abdcdb62
ms.openlocfilehash: 4d2102668b7cc964e6fe3bffdcc6931a2961a737
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50562255"
---
# <a name="user-defined-handlers"></a>사용자 정의 처리기

다음 맵 항목 있는 함수 프로토타입과 일치합니다.

|맵 항목|함수 프로토타입|
|---------------|------------------------|
|ON_MESSAGE ( \<메시지 >, \<memberFxn >)|afx_msg LRESULT memberFxn (WPARAM, LPARAM);|
|ON_REGISTERED_MESSAGE ( \<nMessageVariable >, \<memberFxn >)|afx_msg LRESULT memberFxn (WPARAM, LPARAM);|
|ON_THREAD_MESSAGE ( \<메시지 >, \<memberFxn >)|afx_msg void memberFxn (WPARAM, LPARAM);|
|ON_REGISTERED_THREAD_MESSAGE ( \<nMessageVariable >, \<memberFxn >)|afx_msg void memberFxn (WPARAM, LPARAM);|

## <a name="see-also"></a>참고 항목

[메시지 맵](../../mfc/reference/message-maps-mfc.md)<br/>
[WM_ 메시지 처리기](../../mfc/reference/handlers-for-wm-messages.md)

