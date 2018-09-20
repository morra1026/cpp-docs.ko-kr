---
title: tlbid | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- tlbid
dev_langs:
- C++
helpviewer_keywords:
- tlbid attribute
ms.assetid: 54b06785-191b-4e77-a9a5-485f2b4acb09
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f5bd922089bcf189c403a97679a593a985603a12
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46446259"
---
# <a name="tlbid"></a>tlbid
**C + + 전용**  
  
기본 형식 라이브러리 이외의 라이브러리를 로드할 수 있도록 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
tlbid(number)  
```  
  
### <a name="parameters"></a>매개 변수  
*수*  
`filename`에 있는 형식 라이브러리의 수입니다.  
  
## <a name="remarks"></a>설명  
 
여러 형식 라이브러리를 사용 하 여 기본 형식 라이브러리 이외의 라이브러리를 로드할 수는 단일 DLL에 기본 제공 되는 경우 **tlbid**합니다.  
  
예를 들어:  
  
```  
#import <MyResource.dll> tlbid(2)  
```  
  
다음과 동일합니다.  
  
```  
LoadTypeLib("MyResource.dll\\2");  
```  
  
**C + + 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 
[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)