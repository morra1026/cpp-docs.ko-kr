---
title: '방법: 전역 예외 처리기 정의 및 설치 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- handlers, global
ms.assetid: dd88a812-3bc7-4ce8-8283-4b674c246534
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: ff91a742b1a6641fbc689968587f0472c333e16a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46423366"
---
# <a name="how-to-define-and-install-a-global-exception-handler"></a>방법: 전역 예외 처리기 정의 및 설치

다음 코드 예제에서는 어떻게 처리 되지 않은 예외 캡처할 수 있습니다. 예제에서는 양식에 단추를 누르면 수행 null 참조 예외를 throw 합니다. 이 기능은 일반적인 코드 오류를 나타냅니다. Main 함수에 의해 설치 된 응용 프로그램 수준의 예외 처리기에서 결과 예외가 검색 되었습니다.

이렇게 하려면 대리자를 바인딩하여는 <xref:System.Windows.Forms.Application.ThreadException> 이벤트입니다. 이 경우 후속 예외도 보내집니다는 `App::OnUnhandled` 메서드.

## <a name="example"></a>예제

```
// global_exception_handler.cpp
// compile with: /clr
#using <system.dll>
#using <system.drawing.dll>
#using <system.windows.forms.dll>

using namespace System;
using namespace System::Threading;
using namespace System::Drawing;
using namespace System::Windows::Forms;

ref class MyForm : public Form
{
   Button^ b;
public:
   MyForm( )
   {
      b = gcnew Button( );
      b->Text = "Do Null Access";
      b->Size = Drawing::Size(150, 30);
      b->Click += gcnew EventHandler(this, &MyForm::OnClick);
      Controls->Add(b);
   }
   void OnClick(Object^ sender, EventArgs^ args)
   {
      // do something illegal, like call through a null pointer...
      Object^ o = nullptr;
      o->ToString( );
   }
};

ref class App
{
public:
   static void OnUnhandled(Object^ sender, ThreadExceptionEventArgs^ e)
   {
      MessageBox::Show(e->Exception->Message, "Global Exeception");
      Application::ExitThread( );
   }
};

int main()
{
   Application::ThreadException += gcnew
      ThreadExceptionEventHandler(App::OnUnhandled);

   MyForm^ form = gcnew MyForm( );
   Application::Run(form);
}
```

## <a name="see-also"></a>참고 항목

[예외 처리](../windows/exception-handling-cpp-component-extensions.md)