---
title: ptr::operator bool | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- ptr::operator bool
- ptr.operator bool
- operator bool
- msclr::com::ptr::operator bool
- msclr.com.ptr.operator bool
dev_langs:
- C++
helpviewer_keywords:
- ptr::operator bool
ms.assetid: 31123377-6ecd-4cef-9b75-3db3996fbcd1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: dcccfd23151d2e09f1fcafeb255dd7261ae2c12a
ms.sourcegitcommit: 8480f16893f09911f08a58caf684405404f7ac8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49163792"
---
# <a name="ptroperator-bool"></a>ptr::operator bool

연산자를 사용 하 여 `com::ptr` 조건식에서입니다.

## <a name="syntax"></a>구문

```
operator bool();
```

## <a name="return-value"></a>반환 값

**true** 소유 COM 개체가 잘못 되었습니다. **false** 그렇지 않은 경우.

## <a name="remarks"></a>설명

소유 COM 개체가 없는 경우 올바른 `nullptr`합니다.

이 연산자를 실제로 변환 `_detail_class::_safe_bool` 는 보다 안전한 `bool` 정수 계열 형식으로 변환할 수 없기 때문입니다.

## <a name="example"></a>예제

이 예제에서는 `com::ptr`을 사용해서 해당 개인 멤버 `IXMLDOMDocument` 개체를 래핑하는 CLR 클래스를 구현합니다. 합니다 `CreateInstance` 멤버 함수를 사용 하 여 `operator bool` 경우 유효 하 고 콘솔에 작성 하는 경우를 확인 하려면 새 문서 개체를 만든 후 합니다.

```
// comptr_op_bool.cpp
// compile with: /clr /link msxml2.lib
#include <msxml2.h>
#include <msclr\com\ptr.h>

#import <msxml3.dll> raw_interfaces_only

using namespace System;
using namespace System::Runtime::InteropServices;
using namespace msclr;

// a ref class that uses a com::ptr to contain an
// IXMLDOMDocument object
ref class XmlDocument {
public:
   void CreateInstance(String^ progid) {
      if (!m_ptrDoc) {
         m_ptrDoc.CreateInstance(progid);
         if (m_ptrDoc) { // uses operator bool
            Console::WriteLine("DOM Document created.");
         }
      }
   }

   // note that the destructor will call the com::ptr destructor
   // and automatically release the reference to the COM object

private:
   com::ptr<IXMLDOMDocument> m_ptrDoc;
};

// use the ref class to handle an XML DOM Document object
int main() {
   try {
      XmlDocument doc;
      // create the instance from a progid string
      doc.CreateInstance("Msxml2.DOMDocument.3.0");
   }
   catch (Exception^ e) {
      Console::WriteLine(e);
   }
}
```

```Output
DOM Document created.
```

## <a name="requirements"></a>요구 사항

**헤더 파일** \<msclr\com\ptr.h >

**Namespace** msclr:: com

## <a name="see-also"></a>참고 항목

[ptr 멤버](../dotnet/ptr-members.md)<br/>
[ptr::operator!](../dotnet/ptr-operator-logical-not.md)