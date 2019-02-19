---
title: '변환: 진단'
ms.date: 11/04/2016
ms.assetid: 3730ca7c-0147-452d-bd4a-6a1e97e9793e
ms.openlocfilehash: a274b7c5f29b091b2bf29922abfa4d66d3447b47
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152601"
---
# <a name="translation-diagnostics"></a>변환: 진단

**ANSI 2.1.1.3** 진단 식별 방법

Microsoft C는 다음의 경우에 형식에서 오류 메시지를 생성합니다.

> ‘파일 이름’**(** ‘줄 번호’**):** ‘진단’ **C**<em>번호</em> ‘메시지’

여기서 ‘파일 이름’은 오류가 발견된 소스 파일의 이름이고, ‘줄 번호’는 컴파일러 오류가 발견된 줄 번호이고, ‘진단’은 “오류” 또는 “경고”이고, ‘번호’는 오류 또는 경고를 식별하는 고유한 네 자리 숫자(**C** 뒤에 위치, 구문 설명 참조)이고, ‘메시지’는 설명 메시지입니다.

## <a name="see-also"></a>참고 항목

[구현 정의 ](../c-language/implementation-defined-behavior.md)
