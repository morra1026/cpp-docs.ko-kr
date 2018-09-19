---
title: 컴파일러 경고 (수준 1) C4678 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4678
dev_langs:
- C++
helpviewer_keywords:
- C4678
ms.assetid: 0c588f34-595d-4e5c-9470-8723fca2cc06
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 81eb7df618f97300c2654cc0f4f7a58d18215b26
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076101"
---
# <a name="compiler-warning-level-1-c4678"></a>컴파일러 경고(수준 1) C4678

기본 클래스 'base_type'이 'derived_type'보다 액세스하기 어렵습니다.

public 형식이 전용 형식에서 파생됩니다. 참조된 어셈블리에서 public 형식을 인스턴스화할 경우 전용 기본 형식의 멤버에 액세스할 수 없습니다.

C4678은 사용 되지 않는 컴파일러 옵션을 사용 하 여 연결할 수만 **/clr: oldsyntax**합니다. 사용 하는 경우는 오류 **/clr**, 액세스 하는 기본 클래스는 파생된 클래스입니다.
