---
title: 독립 실행형 특성 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- standalone attributes
- attributes [C++/CLI], standalone
ms.assetid: 0d72e84e-236c-43b3-ac9a-d9b91fcd6794
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5d395053231f54570e1bf86ba79f6237b89681fc
ms.sourcegitcommit: f0c90000125a9497bf61e41624de189a043703c0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44315550"
---
# <a name="stand-alone-attributes"></a>독립 실행형 특성
독립 실행형 특성을 c + + 키워드에서 작동 하지 않습니다 하지만 코드 줄에 비슷합니다. 독립 실행형 특성 문은 줄의 끝에 세미콜론이 필요합니다.
  
|특성|설명|
|---------------|-----------------|
|[cpp_quote](../windows/cpp-quote.md)|생성된 된 헤더 파일의 따옴표 없이 지정된 된 문자열을 내보냅니다.|
|[custom](../windows/custom-cpp.md)|고유한 특성을 정의할 수 있습니다.|
|[db_command](../windows/db-command.md)|OLE DB 명령을 만듭니다.|
|[emitidl](../windows/emitidl.md)|모든 후속 IDL 특성 처리 되어 생성된 된.idl 파일에 배치 될 지 여부를 결정 합니다.|
|[idl_module](../windows/idl-module.md)|DLL에 진입점을 지정합니다.|
|[idl_quote](../windows/idl-quote.md)|Visual c + +의 현재 버전에서 지원 되지 않는 IDL 구문을 사용할 수 있습니다 하 고 생성된 된.idl 파일을 통과 하도록 합니다.|
|[import](../windows/import.md)|주.idl 파일에서 참조 하려는 정의 포함 하는 다른.idl,.odl, 또는.h 파일을 지정 합니다.|
|[importidl](../windows/importidl.md)|생성된 된.idl 파일에 지정 된.idl 파일 삽입|
|[importlib](../windows/importlib.md)|다른 형식 라이브러리에 이미 컴파일된 형식을 만들고 있는 형식 라이브러리에서 사용할 수 있도록 합니다.|
|[include](../windows/include-cpp.md)|생성된 된.idl 파일에 포함할 하나 이상의 헤더 파일을 지정 합니다.|
|[includelib](../windows/includelib-cpp.md)|생성된 된.idl 파일에 포함 될.idl 또는.h 파일을 사용 하면 됩니다.|
|[library_block](../windows/library-block.md)|.Idl 파일의 라이브러리 블록 내부 구문을 배치합니다.|
|[모듈](../windows/module-cpp.md)|.Idl 파일의 라이브러리 블록을 정의합니다.|
|[no_injected_text](../windows/no-injected-text.md)|컴파일러 특성 사용으로 인해 코드를 삽입 하지 못하도록 방지 합니다.|
|[pragma](../windows/pragma.md)|생성된 된.idl 파일의 따옴표 없이 지정된 된 문자열을 내보냅니다.|
  
## <a name="see-also"></a>참고 항목
 [용도별 특성](../windows/attributes-by-usage.md)