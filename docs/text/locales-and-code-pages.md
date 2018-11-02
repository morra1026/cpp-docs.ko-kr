---
title: 로캘 및 코드 페이지
ms.date: 11/04/2016
helpviewer_keywords:
- locales [C++], about locales
- locale IDs [C++]
- locales [C++]
- code pages [C++]
- code pages [C++], dynamically changing
- character sets [C++], code pages
- multibyte code pages [C++]
- character sets [C++], locales
- localization [C++], code pages
- localization [C++], locales
- code pages [C++], locales
- conventions [C++], international character support
ms.assetid: bd937361-b6d3-4c98-af95-beb7c903187b
ms.openlocfilehash: 0015e0a7a81abbd3472a8c845a9b8c0d8caf4618
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50610539"
---
# <a name="locales-and-code-pages"></a>로캘 및 코드 페이지

로캘 ID는 로컬 규칙 및 특정 지리적 지역에 대 한 언어를 반영합니다. 지정된 언어는 여러 국가/지역에서 통용될 수 있습니다. 예를 들어 포르투갈어는 브라질과 포르투갈에서 통용됩니다. 반대로 한 국가/지역에 여러 개의 공식 언어가 있을 수 있습니다. 예를 들어 캐나다는 두 가지 언어: 영어 및 프랑스어입니다. 따라서 캐나다에 두 개의 고유 로캘: 캐나다 영어와 프랑스어 (캐나다). 일부 로캘 종속 범주에는 날짜 형식 지정 및 통화 값의 형식 표시가 포함됩니다.

언어에 따라 텍스트 및 데이터 형식 지정 규칙이 결정되고 국가/지역에 따라 지역 규칙이 결정됩니다. 모든 언어 간의 고유 매핑을, 코드 페이지를 나타내는 문자 (예: 문장 부호 및 숫자) 알파벳에서 이외의 문자를 포함 하는 있습니다. 코드 페이지 문자 집합을 이며 언어와 관련이 있습니다. 따라서 한 [로캘](../c-runtime-library/locale.md) 언어, 국가/지역 및 코드 페이지의 고유한 조합입니다. 호출 하 여 로캘 및 코드 페이지 설정은 런타임 시 변경할 수 있습니다 합니다 [setlocale](../c-runtime-library/reference/setlocale-wsetlocale.md) 함수입니다.

다른 언어는 서로 다른 코드 페이지를 사용할 수 있습니다. 예를 들어 ANSI 코드 페이지 1252는 영어와 대부분의 유럽 언어에 대 한 사용 및 ANSI 코드 페이지 932는 일본어 간지에 사용 됩니다. 거의 모든 코드 페이지는 ASCII 문자는 가장 낮은 128 자 (0x00-0x7F)에 대 한 집합을 공유 합니다.

싱글바이트 코드 페이지 (숫자 및 문장 부호 포함), 문자 또는 문자 모양 바이트 값의 매핑으로 (256 개 항목)이 있는 테이블에 나타낼 수 있습니다. 더블 바이트 문자 값의 매우 큰 테이블 (항목과 64k)으로 모든 멀티 바이트 코드 페이지를 나타낼 수도 있습니다. 그러나 실제이 페이지는 일반적으로 처음 256 (싱글바이트) 문자에 대 한 테이블 더블 바이트 값의 범위로 표현 됩니다.

코드 페이지에 대한 자세한 내용은 [Code Pages](../c-runtime-library/code-pages.md)를 참조하세요.

C 런타임 라이브러리에 두 가지 유형의 내부 코드 페이지: 로캘 및 멀티 바이트입니다. 프로그램 실행 중 현재 코드 페이지를 변경할 수 있습니다 (에 대 한 설명서를 참조 합니다 [setlocale](../c-runtime-library/reference/setlocale-wsetlocale.md) 하 고 [_setmbcp](../c-runtime-library/reference/setmbcp.md) 함수). 또한 런타임 라이브러리를 가져올 하 고 프로그램의 실행 기간에 대 한 상수는 운영 체제 코드 페이지의 값을 사용할 수 있습니다.

로캘 코드 페이지 변경 되는 경우 선택한 코드 페이지에 의해 결정 된 함수 변경 집합이 로캘 종속 동작 합니다. 기본적으로 모든 로캘 종속 함수는 "C" 로캘에서 고유 로캘 코드 페이지를 사용 하 여 실행을 시작 합니다. 내부 로캘 코드 페이지 (뿐만 아니라 다른 로캘에 속성)를 호출 하 여 변경할 수 있습니다는 `setlocale` 함수입니다. 에 대 한 호출 `setlocale`(LC_ALL, "")는 운영 체제 사용자 로캘을 통해 표시 되는 로캘을 설정 합니다.

마찬가지로 변경 되는 경우 멀티 바이트 코드 페이지의 지시 선택한 코드 페이지에 따라 멀티 바이트 함수 변경 내용의 동작입니다. 기본적으로 모든 멀티 바이트 함수는 운영 체제의 기본 코드 페이지에 해당 하는 멀티 바이트 코드 페이지를 사용 하 여 실행을 시작 합니다. 호출 하 여 내부 멀티 바이트 코드 페이지를 변경할 수는 `_setmbcp` 함수입니다.

C 런타임 함수를 `setlocale` 설정, 변경 하거나 일부 또는 모든 현재 프로그램 로캘 정보를 쿼리 합니다. 합니다 [_wsetlocale](../c-runtime-library/reference/setlocale-wsetlocale.md) 루틴의 와이드 문자 버전이 `setlocale`; 인수 및 반환 값의 `_wsetlocale` 는 와이드 문자 문자열입니다.

## <a name="see-also"></a>참고 항목

[유니코드 및 MBCS](../text/unicode-and-mbcs.md)<br/>
[문자 집합 이식성의 이점](../text/benefits-of-character-set-portability.md)