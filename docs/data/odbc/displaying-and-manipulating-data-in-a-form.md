---
title: 폼에서 데이터의 표시와 조작
ms.date: 11/04/2016
helpviewer_keywords:
- forms [C++], displaying data
- displaying data [C++], forms
- ODBC [C++], forms
- record views [C++], displaying data
- data [MFC]
- data [MFC], displaying in a form
ms.assetid: c56185c4-12cb-40b1-b499-02b29ea83e3a
ms.openlocfilehash: 1694d9cbc770e02c550891fc83c1cc0a9f64824a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50517795"
---
# <a name="displaying-and-manipulating-data-in-a-form"></a>폼에서 데이터의 표시와 조작

많은 데이터 액세스 응용 프로그램은 폼의 필드를 이용하여 데이터를 선택하고 표시합니다. [CRecordView](../../mfc/reference/crecordview-class.md) 데이터베이스 클래스는 레코드 집합 개체에 직접 연결되는 [CFormView](../../mfc/reference/cformview-class.md) 개체를 제공합니다. 레코드 뷰는 [대화 상자 데이터 교환(DDX)](../../mfc/dialog-data-exchange-and-validation.md)을 사용하여 레코드 집합에 있는 현재 레코드의 필드 값을 폼의 컨트롤로 이동시키고 업데이트된 정보를 다시 레코드 집합으로 이동시킵니다. 그런 다음 레코드 집합은 레코드 필드 교환(RFX)을 사용하여 자체 필드 데이터 멤버와 데이터 소스에 있는 테이블의 해당 열 사이로 데이터를 이동시킵니다.

MFC 응용 프로그램 마법사나 **클래스 추가**([MFC ODBC 소비자 추가](../../mfc/reference/adding-an-mfc-odbc-consumer.md)의 설명 참조)를 사용하여 뷰 클래스 및 여기에 연결되는 레코드 집합 클래스를 동시에 만들 수 있습니다.

레코드 뷰 및 해당 레코드 집합 문서를 닫을 때 삭제 됩니다. 레코드 뷰에 대 한 자세한 내용은 참조 하세요. [레코드 뷰](../../data/record-views-mfc-data-access.md)합니다. RFX에 대 한 자세한 내용은 참조 하세요. [Exchange RFX (레코드 필드)](../../data/odbc/record-field-exchange-rfx.md)합니다.

## <a name="see-also"></a>참고 항목

[ODBC 및 MFC](../../data/odbc/odbc-and-mfc.md)