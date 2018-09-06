---
title: 호출 예제 결과 | Microsoft Docs
ms.custom: ''
ms.date: 09/05/2018
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- examples [C++], results of calling
- results, thiscall call
- results, __fastcall keyword call
- results, __cdecl call
- results, __stdcall call
ms.assetid: aa70a7cb-ba1d-4aa6-bd0a-ba783da2e642
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5687adfada8657ae26edd9001db8990ff08864e9
ms.sourcegitcommit: d10a2382832373b900b1780e1190ab104175397f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43894697"
---
# <a name="results-of-calling-example"></a>호출 예제 결과

**Microsoft 전용**

## <a name="cdecl"></a>__cdecl
C 데코레이팅된 함수 이름은 `_MyFunc`합니다.

![Cdecl 호출 규칙이](../cpp/media/vc37i01.gif "vc37I01")  
합니다 **__cdecl** 호출 규칙

## <a name="stdcall-and-thiscall"></a>__stdcall 및 thiscall

C 데코레이팅된 이름 (**__stdcall**)은 `_MyFunc@20`합니다. C 데코레이팅된 이름은 구현 별입니다.

![&#95;&#95;stdcall 및 thiscall 호출 규칙](../cpp/media/vc37i02.gif "vc37I02")  
__stdcall 및 thiscall 호출 규칙

## <a name="fastcall"></a>__fastcall

C 데코레이팅된 이름 (**__fastcall**)은 `@MyFunc@20`합니다. C 데코레이팅된 이름은 구현 별입니다.

![호출 규칙에 대 한 &#95; &#95;fastcall](../cpp/media/vc37i03.gif "vc37I03")  
__fastcall 호출 규칙

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[호출 예제: 함수 프로토타입 및 호출](../cpp/calling-example-function-prototype-and-call.md)