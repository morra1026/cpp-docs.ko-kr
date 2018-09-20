---
title: STL/CLR 컨테이너 요소에 대 한 요구 사항 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- C++ Standard Library, template class containers
- STL/CLR, containers
- containers, STL/CLR
- containers, C++ Standard Library
ms.assetid: 59ab240c-15bf-4701-a9f9-e7c56e5ab53f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: fcba36fdf280cef31efb9a84288475fcbb82b291
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46400428"
---
# <a name="requirements-for-stlclr-container-elements"></a>STL/CLR 컨테이너 요소에 대한 요구 사항

STL/CLR 컨테이너에 삽입 되는 모든 참조 형식에 최소한 다음과 같은 요소가 있어야 합니다.

- 공용 복사 생성자입니다.

- 공용 대입 연산자입니다.

- Public 소멸자가 있습니다.

또한 연관 컨테이너와 같은 [설정](../dotnet/set-stl-clr.md) 하 고 [지도](../dotnet/map-stl-clr.md) 되는 공용 비교 연산자 정의 있어야 합니다. `operator<` 기본적으로 합니다. 공용 기본 생성자 및 정의 공용 연산자 컨테이너의 일부 작업 해야 할 수 있습니다.

참조 형식, 값 형식 및 참조 처리와 같은 연관 컨테이너에 삽입할 수 있는 형식 있어야 비교 연산자와 같은 `operator<` 정의 합니다. 공용 복사 생성자, 공용 대입 연산자 및 public 소멸자에 대 한 요구 사항을 참조 형식에는 핸들 또는 값 형식에 대해 존재 하지 않습니다.

## <a name="see-also"></a>참고 항목

[C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)