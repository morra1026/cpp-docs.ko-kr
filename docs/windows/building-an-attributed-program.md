---
title: 특성 사용된 프로그램 빌드 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- tlb files
- MIDL
- MIDL, linker output
- IDL files
- tlb files, building attributed programs
- .tlb files, building attributed programs
- IDL files, building
- attributes [C++], building type libraries and .idl files
- .tlb files
- .idl files, building
- type libraries, linker options for building
ms.assetid: 04997b5f-bf2c-46ec-b868-c4adebbef5f4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7909884a355ccad5e1bf9d18a38dd3e4690296ee
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42587509"
---
# <a name="building-an-attributed-program"></a>특성을 사용하는 프로그램 빌드

소스 코드를 Visual c + + 특성을 추가한 후를 형식 라이브러리 및.idl 파일을 생성 하기 위해 Visual c + + 컴파일러를 확인할 수 있습니다. 다음 링커 옵션.tlb 및.idl 파일을 빌드할 수 있습니다.

- [/IDLOUT](../build/reference/idlout-name-midl-output-files.md)

- [/IGNOREIDL](../build/reference/ignoreidl-don-t-process-attributes-into-midl.md)

- [/ MIDL](../build/reference/midl-specify-midl-command-line-options.md)

- [/TLBOUT](../build/reference/tlbout-name-dot-tlb-file.md)

일부 프로젝트는 여러 독립적인.idl 파일을 포함합니다. 이러한 두 개 이상의.tlb 파일을 생성 하 고 필요에 따라 리소스 블록에 바인딩하고에 사용 됩니다. 이 시나리오는 Visual c + +에서 현재 지원 되지 않습니다.

또한 Visual c + + 링커는 모든 IDL 관련 특성 정보를 단일 MIDL 파일로 출력 합니다. 단일 프로젝트에서 두 개의 형식 라이브러리를 생성할 수 없음이 됩니다.

## <a name="see-also"></a>참고 항목

[개념](../windows/attributed-programming-concepts.md)