---
title: 'marshal_context:: ~ marshal_context | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- marshal_context::~marshal_context
- msclr.interop.marshal_context.~marshal_context
- marshal_context.~marshal_context
- msclr::interop::marshal_context::~marshal_context
- ~marshal_context
dev_langs:
- C++
helpviewer_keywords:
- marshal_context class [C++], operations
ms.assetid: 34c41b38-4c33-4f61-b74e-831ac46b4ab5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 49f194f153f3e4f911333e22b11ebddf7efcaa32
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46447260"
---
# <a name="marshalcontextmarshalcontext"></a>marshal_context::~marshal_context

`marshal_context` 개체를 제거합니다.

## <a name="syntax"></a>구문

```
~marshal_context();
```

## <a name="remarks"></a>설명

일부 데이터 변환을 마샬링 컨텍스트가 필요 합니다. 참조 [Overview of Marshaling c + +에서](../dotnet/overview-of-marshaling-in-cpp.md) 는 번역 컨텍스트 하며 응용 프로그램에 포함할 마샬링 파일에 대 한 자세한 내용은 합니다.

삭제를 `marshal_context` 개체 컨텍스트에서 변환 데이터를 무효화 됩니다. 이후에 데이터를 보존 하려는 경우를 `marshal_context` 개체 삭제 되 면 유지 되는 변수에 데이터를 수동으로 복사 해야 합니다.

## <a name="requirements"></a>요구 사항

**헤더 파일:** \<msclr\marshal.h >, \<msclr\marshal_windows.h >, \<msclr\marshal_cppstd.h >, 또는 \<msclr\marshal_atl.h >

**Namespace:** msclr::interop

## <a name="see-also"></a>참고 항목

[C++ 마샬링 개요](../dotnet/overview-of-marshaling-in-cpp.md)<br/>
[marshal_as](../dotnet/marshal-as.md)<br/>
[marshal_context 클래스](../dotnet/marshal-context-class.md)