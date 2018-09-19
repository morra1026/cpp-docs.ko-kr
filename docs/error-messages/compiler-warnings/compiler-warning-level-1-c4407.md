---
title: 컴파일러 경고 (수준 1) C4407 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4407
dev_langs:
- C++
helpviewer_keywords:
- C4407
ms.assetid: 32bc2c21-363a-4bb8-b486-725faeaededc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a9a665dbb71157b37f72d3d0721357d00dc37230
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032605"
---
# <a name="compiler-warning-level-1-c4407"></a>컴파일러 경고(수준 1) C4407

멤버 표현이 다른 포인터를 간의 캐스팅, 컴파일러 발생할 잘못 된 코드

잘못 된 캐스트가 발견 되었습니다.

Visual c + + 2005에서 수행 된 컴파일러 규칙 작업으로 인해 C4407은 생성할 수 있습니다. 이제 멤버 포인터에 정규화된 이름과 연산자 주소(&)가 필요합니다.

C4407 간에 여러 상속-멤버 포인터는 단일 상속 포인터 멤버를 캐스팅 하는 경우에 발생할 수 있습니다. 경우에 따라이 작동할 수 하지만 경우에 따라 만들 수 없습니다 단일 상속 멤버 포인터 표현 충분 한 정보를 저장 하지 않습니다. 사용 하 여 컴파일하는 **/vmm** 도움이 될 수 있습니다 (자세한 내용은 참조 하십시오 [/vmm, /vms, /vmv (일반적인 용도 표시)](../../build/reference/vmm-vms-vmv-general-purpose-representation.md)). 기본 클래스;를 다시 정렬 시도해 볼 수 있습니다. 컴파일러 기본 클래스 로부터 파생 된 0이 아닌 오프셋 때문에 변환에 정보가 손실을 감지 됩니다.

다음 샘플에서는 C4407 오류가 생성 됩니다.

```
// C4407.cpp
// compile with: /W1 /c
struct C1 {};
struct C2 {};
struct C3 : C1, C2 {};

typedef void(C3::*PMF_C3)();
typedef void(C2::*PMF_C2)();

PMF_C2 f1(PMF_C3 pmf) {
   return (PMF_C2)pmf;   // C4407, change type of cast,
   // or reverse base class inheritance of C3 (i.e. : C2, C1)
}
```