---
title: 속성 추가 마법사, IDL 특성 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- vc.codewiz.prop.idlattributes
dev_langs:
- C++
ms.assetid: 356ed666-79d0-4bd9-a5e7-cda679cbadbd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ce3597f656d46da85faee3f6ec51b89257d25d05
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46426356"
---
# <a name="idl-attributes-add-property-wizard"></a>속성 추가 마법사, IDL 특성

이 속성에 대한 IDL(인터페이스 정의 언어) 설정을 지정하려면 이 속성 추가 마법사 페이지를 사용합니다.

- **ID**

   속성을 식별하는 숫자 ID를 설정합니다. 이 옵션은 사용자 지정 인터페이스의 속성에 사용할 수 없습니다. *MIDL 참조*에서 [id](/windows/desktop/Midl/id)를 확인합니다.

- **helpcontext**

   도움말 파일에서 이 속성에 대한 정보를 볼 수 있는 컨텍스트 ID를 지정합니다. *MIDL 참조*에서 [helpcontext](/windows/desktop/Midl/helpcontext)를 확인합니다.

- **helpstring**

   적용되는 요소를 설명하는 데 사용되는 문자열을 지정합니다. 기본적으로 "속성 *속성 이름*"으로 설정됩니다. *MIDL 참조*에서 [helpstring](/windows/desktop/Midl/helpstring)을 확인합니다.

## <a name="other-options"></a>기타 옵션

일부 옵션은 모든 속성 유형에 대해 사용할 수 있습니다.

|옵션|설명|
|------------|-----------------|
|**bindable**|속성이 데이터 바인딩을 지원합니다. *MIDL 참조*에서 [bindable](/windows/desktop/Midl/bindable)을 확인합니다. 속성의 스톡 구현의 경우 기본적으로 이 옵션이 설정되며 변경할 수 없습니다.|
|**defaultbind**|개체를 가장 잘 나타내는 하나의 바인딩할 수 있는 속성입니다. *MIDL 참조*에서 [defaultbind](/windows/desktop/Midl/defaultbind)를 확인합니다.|
|**displaybind**|사용자에게 바인딩할 수 있는 속성으로 표시합니다. *MIDL 참조*에서 [displaybind](/windows/desktop/Midl/displaybind)를 확인합니다.|
|**immediatebind**|데이터 바인딩된 개체의 이 속성에 대한 모든 변경 내용을 데이터베이스에 즉시 알립니다. *MIDL 참조*에서 [immediatebind](/windows/desktop/Midl/immediatebind)를 확인합니다.|
|**defaultcollelem**|속성은 기본 컬렉션의 요소에 대한 접근자 함수입니다. *MIDL 참조*에서 [defaultcollelem](/windows/desktop/Midl/defaultcollelem)을 확인합니다.|
|**nonbrowsable**|속성 브라우저에 표시하지 않아야 할 인터페이스 또는 dispinterface 멤버를 태그합니다. *MIDL 참조*에서 [nonbrowsable](/windows/desktop/Midl/nonbrowsable)을 확인합니다.|
|**requestedit**|속성이 **OnRequestEdit** 알림을 지원합니다. *MIDL 참조*에서 [requestedit](/windows/desktop/Midl/requestedit)을 확인합니다. 속성의 스톡 구현의 경우 기본적으로 이 옵션이 설정되며 변경할 수 없습니다.|
|**source**|속성의 멤버가 이벤트의 소스입니다. *MIDL 참조*에서 [source](/windows/desktop/Midl/source)를 확인합니다.|
|**hidden**|속성이 존재하지만 사용자 기반 브라우저에는 표시되지 않아야 합니다. *MIDL 참조*에서 [hidden](/windows/desktop/Midl/hidden)을 확인합니다.|
|**restricted**|임의로 속성을 호출할 수 없도록 지정합니다. *MIDL 참조*에서 [restricted](/windows/desktop/Midl/restricted)를 확인합니다.|
|`local`|속성이 원격이 아니라고 MIDL 컴파일러에 지정합니다. *MIDL 참조*에서 [local](/windows/desktop/Midl/local)을 확인합니다.|

## <a name="see-also"></a>참고 항목

[속성 추가](../ide/adding-a-property-visual-cpp.md)<br>
[속성 추가 마법사, 이름](../ide/names-add-property-wizard.md)<br>
[인터페이스 구현](../ide/implementing-an-interface-visual-cpp.md)<br>
[스톡 속성](../ide/stock-properties.md)