---
title: no_namespace | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- no_namespace
dev_langs:
- C++
helpviewer_keywords:
- no_namespace attribute
ms.assetid: 5d81b741-a558-451b-b493-1f3b18967337
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6eded6b4d543248cc7bf53a0e4ba622b2b74c8b3
ms.sourcegitcommit: d4c803bd3a684d7951bf88dcecf1f14af43ae411
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/10/2018
ms.locfileid: "42539662"
---
# <a name="nonamespace"></a>no_namespace
**C + + 전용**  
  
컴파일러가 생성하지 않은 네임스페이스 이름을 지정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
no_namespace  
```  
  
## <a name="remarks"></a>설명  
 
`#import` 헤더 파일의 형식 라이브러리 콘텐츠는 일반적으로 네임스페이스에 정의됩니다. 네임 스페이스 이름에 지정 된 된 `library` 원본 IDL 파일의 문입니다. 경우는 **no_namespace** 특성을 지정 하면 다음이 네임 스페이스는 컴파일러에서 생성 되지 않습니다.  
  
다른 네임 스페이스 이름을 사용 하려는 경우 사용 합니다 [rename_namespace](../preprocessor/rename-namespace.md) 특성을 대신 합니다.  
  
**C + + 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 
[#import 특성](../preprocessor/hash-import-attributes-cpp.md)   
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)