---
title: 컴파일러 COM 전역 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- cl.exe compiler, COM support
- COM, compiler support
ms.assetid: 74449d26-50a2-47c7-b175-7cf2cf83533e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: cb769cf1419f7a0142a5eeae348ca432f78fb92a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46034143"
---
# <a name="compiler-com-global-functions"></a>컴파일러 COM 전역 함수

**Microsoft 전용**

다음 루틴을 사용할 수 있습니다.

|기능|설명|
|--------------|-----------------|
|[_com_raise_error](../cpp/com-raise-error.md)|Throw 된 [_com_error](../cpp/com-error-class.md) 오류에 대 한 응답에서입니다.|
|[_set_com_error_handler](../cpp/set-com-error-handler.md)|COM 오류 처리에 사용되는 기본 함수를 대체합니다.|
|[ConvertBSTRToString](../cpp/convertbstrtostring.md)|변환 된 `BSTR` 값을 `char *`.|
|[ConvertStringToBSTR](../cpp/convertstringtobstr.md)|변환 된 `char *` 값을 `BSTR`.|

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[컴파일러 COM 지원 클래스](../cpp/compiler-com-support-classes.md)<br/>
[컴파일러 COM 지원](../cpp/compiler-com-support.md)