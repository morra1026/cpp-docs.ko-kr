---
title: __based 문법 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- based addressing
ms.assetid: a68ff750-c7fa-4c0c-8d5f-2df76e4686c5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 43e9074de25d8cb914432123478f5f338ff4ba1e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103771"
---
# <a name="based-grammar"></a>__based 문법

## <a name="microsoft-specific"></a>Microsoft 전용

기반 주소 지정은 개체가 할당된(정적 및 동적 기반 데이터) 세그먼트를 정밀하게 제어해야 할 때 유용합니다.

기반 주소 지정의 32 비트 및 64 비트 컴파일 허용 되는 "포인터 기반" 유일한 형식에 따라 또는 32 비트 또는 64 비트 자료에는 32 비트 또는 64 비트 치환을 포함 하는 형식 정의 하는 **void**합니다.

## <a name="grammar"></a>문법

*범위 기반-한정자*: **__based (***자료 식***)** 

*기본 식*: *based-variablebased-abstract-declaratorsegment-namesegment-cast*

*기반 변수*: *식별자*

*기반-추상 선언 자*: *추상 선언 자*

*기본 형식*: *형식-이름*

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[기반 포인터](../cpp/based-pointers-cpp.md)