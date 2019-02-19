---
title: 와일드카드 인수 확장명
ms.date: 11/04/2016
helpviewer_keywords:
- asterisk wildcard
- question mark, wildcard
- expanding wildcard arguments
- wildcards, expanding
ms.assetid: 80a11c4b-0199-420e-a342-cf1d803be5bc
ms.openlocfilehash: f1fb964fe98223fb7187b83c7101027ed1f9cbea
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56149052"
---
# <a name="expanding-wildcard-arguments"></a>와일드카드 인수 확장명

**Microsoft 전용**

C 프로그램을 실행할 때 물음표(?)와 별표(*) 중 하나를 와일드카드로 사용하여 명령줄에서 파일 이름 및 경로 인수를 지정할 수 있습니다.

기본적으로 명령줄 인수에서는 와일드카드가 확장되지 않습니다. 일반 인수 벡터 `argv` 로드 루틴을 setargv.obj 또는 wsetargv.obj 파일과 연결하여 와일드카드를 확장하는 버전으로 바꿀 수 있습니다. 프로그램에서 `main` 함수를 사용하는 경우 setargv.obj와 연결합니다. 프로그램에서 `wmain` 함수를 사용하는 경우 wsetargv.obj와 연결합니다. 이 두 동작은 동일한 동작입니다.

setargv.obj 또는 wsetargv.obj와 연결하려면 **/link** 옵션을 사용합니다. 예:

**cl example.c /link setargv.obj**

운영 체제 명령과 같은 방식으로 와일드카드가 확장됩니다. 와일드카드에 대해 잘 모를 경우 운영 체제 사용자 가이드를 참조하십시오.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고 항목

[링크 옵션](../c-runtime-library/link-options.md)<br/>
[main 함수 및 프로그램 실행](../c-language/main-function-and-program-execution.md)
