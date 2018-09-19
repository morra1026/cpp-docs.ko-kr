---
title: 생성자 초기화 순서에서 변경 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- constructors, C++
ms.assetid: 8892c38d-6bf7-4cf7-ac8f-15e052135a79
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: fd54e9810131f3ddfabe458c70ddef081568a9cd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46397691"
---
# <a name="changes-in-constructor-initialization-order"></a>생성자 초기화 순서 변경 사항

클래스 생성자 초기화 순서에 Visual c + + Managed Extensions for c + + 변경 되었습니다.

## <a name="comparison-of-constructor-initialization-order"></a>생성자 초기화 순서 비교

Managed extensions for c + + 생성자 초기화는 다음과 같은 순서로 발생 했습니다.

1. 기본 클래스의 생성자 있으면 호출 됩니다.

1. 클래스 초기화 목록 평가 됩니다.

1. 클래스 생성자의 코드 본문에서 실행 됩니다.

이 실행 순서는 네이티브 c + + 프로그래밍와 같이 동일한 규칙을 따릅니다. 새 Visual c + + 언어는 CLR 클래스에 대 한 다음 실행 순서를 각자:

1. 클래스 초기화 목록 평가 됩니다.

1. 기본 클래스의 생성자 있으면 호출 됩니다.

1. 클래스 생성자의 코드 본문에서 실행 됩니다.

참고가이 변경 내용은 CLR 클래스에만 적용 됩니다. Visual c + +에서 네이티브 클래스는 여전히 이전 규칙을 따릅니다. 두 경우 모두 이러한 규칙 상향 지정된 된 클래스의 전체 계층 구조 체인 전체에서 연계 합니다.

Managed Extensions for c + + 사용 하 여 다음 코드 예제를 살펴보세요.

```
__gc class A
{
public:
   A() : _n(1)
   {
   }

protected:
   int _n;
};

__gc class B : public A
{
public:
   B() : _m(_n)
   {
   }
private:
   int _m;
};
```

위에서 설명한 생성자 초기화 순서에 따르면, 새 실행의 다음 순서를 확인할 클래스의 인스턴스 `B` 생성 됩니다.

1. 기본 클래스의 생성자 `A` 가 호출 됩니다. 합니다 `_n` 멤버가로 초기화 됩니다 `1`합니다.

1. 클래스에 대 한 초기화 목록 `B` 평가 됩니다. 합니다 `_m` 멤버가로 초기화 됩니다 `1`합니다.

1. 클래스의 코드 본문 `B` 실행 됩니다.

이제 새로운 Visual c + + 구문에서 동일한 코드를 고려 합니다.

```
ref class A
{
public:
   A() : _n(1)
   {
   }

protected:
   int _n;
};

ref class B : A
{
public:
   B() : _m(_n)
   {
   }
private:
   int _m;
};
```

새 실행 순서 클래스의 인스턴스 `B` 새에서 생성 된 구문:

1. 클래스에 대 한 초기화 목록 `B` 평가 됩니다. 합니다 `_m` 멤버가로 초기화 됩니다 `0` (`0` 초기화 되지 않은 값인를 `_m` 클래스 멤버).

1. 기본 클래스의 생성자 `A` 가 호출 됩니다. 합니다 `_n` 멤버가로 초기화 됩니다 `1`합니다.

1. 클래스의 코드 본문 `B` 실행 됩니다.

비슷한 구문을 이러한 코드 예제에 대 한 서로 다른 결과 생성 하는 참고 합니다. 클래스의 생성자 `B` 기본 클래스의 값에 따라 달라 집니다 `A` 해당 멤버를 초기화 합니다. 그러나 클래스의 생성자 `A` 가 아직 호출 되지 않았습니다. 상속된 된 클래스는 기본 클래스 생성자에서 발생 하는 메모리 또는 리소스 할당에 따라 다른 경우 이러한 종속성은 특히 위험할 수 있습니다.

## <a name="what-this-means-going-from-managed-extensions-for-c-to-visual-c-2010"></a>Managed Extensions에서 Visual c + + 2010으로 c + +에 대 한 이동이 어떤 의미

대부분의 경우에서 기본 클래스에 상속 된 클래스의 동작 개념이 없으므로 있으므로 클래스 생성자의 실행 순서를 변경 프로그래머에 게 투명 하 게 이어야 합니다. 그러나 이러한 코드 예제에서 알 수 있듯이 상속 된 클래스의 생성자 달라질 수 있습니다 크게 때 해당 초기화 목록을 기본 클래스 멤버의 값에 따라 달라 집니다. 코드에서 Managed Extensions for c + + 새 구문을 이동 하는 경우 실행 마지막으로 발생 하도록 보장 되는 클래스 생성자의 본문에 이러한 구문을 이동 하는 것이 좋습니다.

## <a name="see-also"></a>참고 항목

[관리 되는 형식 (C + + /cli CL)](../dotnet/managed-types-cpp-cl.md)<br/>
[생성자](../cpp/constructors-cpp.md)
