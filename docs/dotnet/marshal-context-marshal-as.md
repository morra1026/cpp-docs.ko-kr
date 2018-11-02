---
title: marshal_context::marshal_as
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- marshal_context::marshal_as
- marshal_context.marshal_as
- msclr.interop.marshal_context.marshal_as
- msclr::interop::marshal_context::marshal_as
helpviewer_keywords:
- marshal_context class [C++], operations
ms.assetid: 24a1afee-51c0-497c-948c-f77fe43635c8
ms.openlocfilehash: b097fda0870b2f49d4883e0fafd48f9637d28853
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50649777"
---
# <a name="marshalcontextmarshalas"></a>marshal_context::marshal_as

특정 데이터 개체를 관리 및 네이티브 데이터 형식 간에 변환할 마샬링을 수행 합니다.

## <a name="syntax"></a>구문

```
To_Type marshal_as<To_Type>(
   From_Type input
);
```

#### <a name="parameters"></a>매개 변수

*input*<br/>
[in] 에 마샬링하 려는 값을 `To_Type` 변수입니다.

## <a name="return-value"></a>반환 값

형식 변수의 `To_Type` 으로 변환된 된 값 즉 `input`합니다.

## <a name="remarks"></a>설명

이 함수는 특정 데이터 개체의 마샬링을 수행 합니다. 이 함수를 사용 하 여 테이블에서 지정 된 변환 만으로 [Overview of Marshaling c + +에서](../dotnet/overview-of-marshaling-in-cpp.md)합니다.

지원 되지 않는 데이터 형식의 쌍 마샬링할 하려고 하면 `marshal_as` 오류가 생성 됩니다 [C4996](../error-messages/compiler-warnings/compiler-warning-level-3-c4996.md) 컴파일 타임에 있습니다. 자세한 내용은이 오류와 함께 제공 되는 메시지를 읽습니다. `C4996` 이상만 사용 되지 않는 함수에 대 한 오류를 생성할 수 있습니다. 이 오류를 생성 하는 두 가지 조건은를 지원 하지 않는 데이터 형식의 한 쌍을 마샬링하는 동안 하며 사용 하는 동안 `marshal_as` 필요한 컨텍스트를 변환 합니다.

마샬링 라이브러리는 몇 가지 헤더 파일의 구성 됩니다. 변환 파일을 하나만 이어야 하는데 다른 변환 해야 할 경우 추가 파일을 포함할 수 있습니다. 표의 `Marshaling Overview in C++` 나타냅니다 마샬링 파일 각 변환에 포함 해야 합니다.

## <a name="example"></a>예제

마샬링에 대 한 컨텍스트를 만드는이 예제는 `System::String` 에 `const char *` 변수 형식입니다. 변환된 된 데이터 컨텍스트를 삭제 하는 줄 뒤 잘못 되지 않습니다.

```
// marshal_context_test.cpp
// compile with: /clr
#include <stdlib.h>
#include <string.h>
#include <msclr\marshal.h>

using namespace System;
using namespace msclr::interop;

int main() {
   marshal_context^ context = gcnew marshal_context();
   String^ message = gcnew String("Test String to Marshal");
   const char* result;
   result = context->marshal_as<const char*>( message );
   delete context;
   return 0;
}
```

## <a name="requirements"></a>요구 사항

**헤더 파일:** \<msclr\marshal.h >, \<msclr\marshal_windows.h >, \<msclr\marshal_cppstd.h >, 또는 \<msclr\marshal_atl.h >

**Namespace:** msclr::interop

## <a name="see-also"></a>참고 항목

[C++ 마샬링 개요](../dotnet/overview-of-marshaling-in-cpp.md)<br/>
[marshal_as](../dotnet/marshal-as.md)<br/>
[marshal_context 클래스](../dotnet/marshal-context-class.md)