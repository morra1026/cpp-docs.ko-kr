---
title: 컴파일러 경고 (수준 1) C4621 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4621
dev_langs:
- C++
helpviewer_keywords:
- C4621
ms.assetid: 40931bd9-cb89-497e-86f0-cec9f016c63c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 70b9273e1c3a91db37be6bee2c1c33a0a4e30b17
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46090830"
---
# <a name="compiler-warning-level-1-c4621"></a>컴파일러 경고(수준 1) C4621

'operator--' 접두사 형식을 사용 하 여 ' type' 형식에 대해 찾을의 후 위 형식이 없으므로

지정된 된 형식에 대해 정의 된 후 위 감소 연산자 있었습니다. 컴파일러가 오버로드된 전위 연산자를 사용했습니다.

후 위를 정의 하 여이 경고를 방지할 수 있습니다 `--` 연산자입니다. 인수가 두 개인 버전을 만들는 `--` 아래와 같이 연산자:

```
// C4621.cpp
// compile with: /W1
class A
{
public:
   A(int nData) : m_nData(nData)
   {
   }

   A operator--()
   {
      m_nData -= 1;
      return *this;
   }

   // A operator--(int)
   // {
   //    A tmp = *this;
   //    m_nData -= 1;
   //    return tmp;
   // }

private:
   int m_nData;
};

int main()
{
   A a(10);
   --a;
   a--;   // C4621
}
```