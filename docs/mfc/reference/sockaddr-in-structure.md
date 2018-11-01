---
title: SOCKADDR_IN 구조체
ms.date: 11/04/2016
f1_keywords:
- SOCKADDR_IN
helpviewer_keywords:
- SOCKADDR_IN structure [MFC]
ms.assetid: e8cd7c34-78bd-4e28-a990-eb3ca070b7a6
ms.openlocfilehash: 22d02b2e3c6fd7151e59cad0f3233539c04a16e0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50431228"
---
# <a name="sockaddrin-structure"></a>SOCKADDR_IN 구조체

인터넷 주소 제품군에는 `SOCKADDR_IN` 구조를 사용 하 여 Windows 소켓 소켓을 연결 하는 데 로컬 또는 원격 끝점 주소를 지정 합니다.

## <a name="syntax"></a>구문

```
struct sockaddr_in{
    short sin_family;
    unsigned short sin_port;
struct in_addr sin_addr;
    char sin_zero[8];
};
```

#### <a name="parameters"></a>매개 변수

*sin_family*<br/>
주소 패밀리 (AF_INET 이어야 함)입니다.

*sin_port*<br/>
IP 포트입니다.

*sin_addr*<br/>
IP 주소입니다.

*sin_zero*<br/>
동일한 크기의 구조를 만들기 위한 패딩 `SOCKADDR`합니다.

## <a name="remarks"></a>설명

형식은이 `SOCKADDR` 인터넷 주소 제품군에 특정 구조체이 고 캐스팅할 수 `SOCKADDR`입니다.

이 구조체의 IP 주소 구성 요소가 형식 `IN_ADDR`합니다. `IN_ADDR` 구조 WINSOCK Windows 소켓 헤더 파일에 정의 되어 있습니다. 다음과 같이 H:

```
struct in_addr {
    union {
        struct {
            unsigned char s_b1, s_b2, s_b3, s_b4;
        } S_un_b;
        struct {
            unsigned short s_w1, s_w2;
        } S_un_w;
        unsigned long S_addr;
    } S_un;
};
```

## <a name="requirements"></a>요구 사항

**헤더:** winsock2.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[SOCKADDR 구조체](../../mfc/reference/sockaddr-structure.md)
