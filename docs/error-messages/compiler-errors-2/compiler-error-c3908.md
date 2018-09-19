---
title: 컴파일러 오류 C3908 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3908
dev_langs:
- C++
helpviewer_keywords:
- C3908
ms.assetid: 3c322482-c79e-4197-a578-2ad9bc379d1a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7591b8ab5f8495b6af866e23e7a169b0f9cd29a6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047319"
---
# <a name="compiler-error-c3908"></a>컴파일러 오류 C3908

'construct' 보다 덜 제한적인 액세스 수준

속성 접근자 메서드 (get 또는 set)는 자체 속성에 대 한 액세스를 보다 덜 제한적인 액세스를 가질 수 없습니다.  경우에 마찬가지 이벤트 접근자 메서드.

자세한 내용은 [속성](../../windows/property-cpp-component-extensions.md) 하 고 [이벤트](../../windows/event-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3908를 생성합니다.

```
// C3908.cpp
// compile with: /clr
ref class X {
protected:
   property int i {
   public:   // C3908 property i is protected
      int get();
   private:
      void set(int);   // OK more restrictive
   };
};
```