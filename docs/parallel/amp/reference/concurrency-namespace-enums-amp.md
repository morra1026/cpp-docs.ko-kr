---
title: Concurrency 네임 스페이스 열거형 (AMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- amp/Concurrency::access_type
- amp/Concurrency::queuing_mode
dev_langs:
- C++
ms.assetid: 4c87457e-184f-4992-81ab-ca75e7d524ab
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d4f842b799a81179fa1a612e652aae391ca3375d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46435664"
---
# <a name="concurrency-namespace-enums-amp"></a>Concurrency 네임 스페이스 열거형 (AMP)

|||
|-|-|
|[access_type 열거형](#access_type)|[queuing_mode 열거형](#queuing_mode)|

##  <a name="access_type"></a>  access_type 열거형

다양 한 유형의 데이터에 대 한 액세스를 나타내는 데 사용 되는 열거형 형식입니다.

```
enum access_type;
```
### <a name="values"></a>값

|이름|설명|
|----------|-----------------|
|`access_type_auto`|자동으로 최상의 선택 `access_type` 액셀러레이터 키에 대 한 합니다.|
|`access_type_none`|집중적으로 다루었습니다. 할당은 CPU 아닌 액셀러레이터 키에 액세스할 수만 있습니다.|
|`access_type_read`|공유 합니다. 할당은 액셀러레이터 키에 액세스할 수 있으며 CPU에서 읽을 수 있는 합니다.|
|`access_type_read_write`|공유 합니다. 할당은 액셀러레이터 키에 액세스할 수 있으며 CPU에서 쓸 수입니다.|
|`access_type_write`|공유 합니다. 할당은 액셀러레이터 키에 액세스할 수 있으며 읽고 CPU에서 쓸 수 있는 합니다.|

##  <a name="queuing_mode"></a>  queuing_mode 열거형

액셀러레이터 키에서 지원 되는 큐 모드를 지정 합니다.

```
enum queuing_mode;
```
### <a name="values"></a>값

|이름|설명|
|----------|-----------------|
|`queuing_mode_immediate`|예를 들어 큐 모드를 지정 하는 명령 [parallel_for_each 함수 (c + + AMP)](concurrency-namespace-functions-amp.md#parallel_for_each)를 호출자에 게 반환 되는 즉시 해당 가속기 장치로 보내집니다.|
|`queuing_mode_automatic`|명령에 해당 하는 명령 큐에 대기 수를 지정 하는 큐 모드를 [accelerator_view](accelerator-view-class.md) 개체입니다. 명령을 장치로 전송 된 경우 [accelerator_view:: flush](accelerator-view-class.md#flush) 라고 합니다.|

## <a name="see-also"></a>참고 항목

[Concurrency 네임스페이스(C++ AMP)](concurrency-namespace-cpp-amp.md)
