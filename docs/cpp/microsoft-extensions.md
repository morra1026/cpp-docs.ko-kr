---
title: Microsoft 확장 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- Microsoft extensions to C/C++
ms.assetid: 68654516-24ef-4f33-aae2-175f86cc1979
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5699ce82a6e8537f12da50fdcb8288da167ecca3
ms.sourcegitcommit: 92dbc4b9bf82fda96da80846c9cfcdba524035af
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43752241"
---
# <a name="microsoft-extensions"></a>Microsoft 확장명

*asm 문*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__asm***어셈블리 명령* **;** <sub>최적화  </sub><br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__asm {***어셈블리 명령 목록***};** <sub>최적화    </sub>

*어셈블리 명령 목록*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*어셈블리 명령* **;** <sub>최적화</sub> <br/>
&nbsp;&nbsp;&nbsp;&nbsp;*어셈블리 명령* **;** *어셈블리 명령 목록* **;** <sub>최적화</sub>

*ms 한정자 목록*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*ms 한정자* *ms 한정자 목록*<sub>최적화</sub>

*ms 한정자*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__cdecl**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__fastcall**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__stdcall**<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__syscall** (이후 구현을 위해 예약 됨)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__oldcall** (이후 구현을 위해 예약 됨)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__unaligned** (이후 구현을 위해 예약 됨)<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*기반 한정자*

*기반 한정자*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**__based (** *기반으로 형식당* **)**

*형식 기반*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*이름*