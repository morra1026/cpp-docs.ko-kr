---
title: 't:: typeid Typeof | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- typeid operator
- __typeof keyword
- typeid keyword [C++]
ms.assetid: 6a0d35a7-7a1a-4070-b187-cff37cfdc205
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 4433061fceef455685b6588c81c8c2e434253433
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46374680"
---
# <a name="typeof-goes-to-ttypeid"></a>typeof 대신 T::typeid 사용

합니다 `typeof` c + +로 변경 된가 데 Managed Extensions에 사용할 연산자를 `typeid` Visual c + +에서 키워드입니다.

Managed extensions에서는 `__typeof()` 연산자는 연결 된 반환 `Type*` 의 관리 되는 형식 이름을 전달 하는 경우 개체입니다. 예를 들어:

```
// Creates and initializes a new Array instance.
Array* myIntArray =
   Array::CreateInstance( __typeof(Int32), 5 );
```

새 구문의 `__typeof` 라는 추가 형식으로 대체 되었습니다 `typeid` 반환 하는 `Type^` 관리 되는 형식 지정 된 경우.

```
// Creates and initializes a new Array instance.
Array^ myIntArray =
   Array::CreateInstance( Int32::typeid, 5 );
```

## <a name="see-also"></a>참고 항목

[일반적인 언어 변경 사항(C++/CLI)](../dotnet/general-language-changes-cpp-cli.md)<br/>
[typeid](../windows/typeid-cpp-component-extensions.md)