---
title: Platform, default 및 cli 네임 스페이스 (C + + /cli 및 C + + /cli CX)
ms.date: 10/12/2018
ms.topic: reference
f1_keywords:
- lang
- cli
helpviewer_keywords:
- lang namespace
- cli namespace
ms.assetid: 9d38bd1e-dc78-47d1-a84b-9b4683e52c9c
ms.openlocfilehash: fb7c9135051d790a488775451e1d333ce69d3dda
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50598006"
---
# <a name="platform-default-and-cli-namespaces--ccli-and-ccx"></a>Platform, default 및 cli 네임 스페이스 (C + + /cli 및 C + + /cli CX)

네임스페이스는 언어 요소의 이름을 한정하므로, 이름이 그렇지 않았다면 소스 코드의 다른 곳에 있는 같은 이름과 충돌하지 않습니다. 예를 들어 이름 충돌이 방해가 컴파일러에서 인식 [상황에 맞는 키워드](../windows/context-sensitive-keywords-cpp-component-extensions.md)합니다. 네임스페이스는 컴파일러에 의해 사용되지만 컴파일된 어셈블리에 유지되지 않습니다.

## <a name="all-runtimes"></a>모든 런타임

Visual Studio 프로젝트를 만들 때 프로젝트에 대 한 기본 네임 스페이스를 제공 합니다. 하지만에서 C + 네임 스페이스 이름을 수동으로 바꿀 수 있습니다 + CX.winmd 파일의 이름에는 루트 네임 스페이스의 이름과 일치 해야 합니다.

## <a name="windows-runtime"></a>Windows 런타임

자세한 내용은 [네임 스페이스 및 형식 표시 유형 (C + + /cli CX)](https://msdn.microsoft.com/library/windows/apps/hh969551.aspx)합니다.

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/ZW`

## <a name="common-language-runtime"></a>공용 언어 런타임

### <a name="syntax"></a>구문

```cpp
using namespace cli;
```

### <a name="remarks"></a>설명

C + + /cli CLI를 지원 합니다 **cli** 네임 스페이스입니다. 사용 하 여 컴파일하면 `/clr`, **를 사용 하 여** 구문 섹션에서 문 인 것으로 간주 합니다.

다음 언어 기능에는 **cli** 네임 스페이스:

- [배열](../windows/arrays-cpp-component-extensions.md)

- [interior_ptr(C++/CLI)](../windows/interior-ptr-cpp-cli.md)

- [pin_ptr(C++/CLI)](../windows/pin-ptr-cpp-cli.md)

- [safe_cast](../windows/safe-cast-cpp-component-extensions.md)

### <a name="requirements"></a>요구 사항

컴파일러 옵션: `/clr`

### <a name="examples"></a>예제

다음 코드 예제에서 기호를 사용할 수 있다는 것을 보여 줍니다.는 **cli** 코드에서 사용자 정의 기호로 네임 스페이스입니다.  그러나이 작업을 수행한 후 해야 명시적 또는 암시적으로 한정에 대 한 참조를 **cli** 이름이 같은 언어 요소입니다.

```cpp
// cli_namespace.cpp
// compile with: /clr
using namespace cli;
int main() {
   array<int> ^ MyArray = gcnew array<int>(100);
   int array = 0;

   array<int> ^ MyArray2 = gcnew array<int>(100);   // C2062

   // OK
   cli::array<int> ^ MyArray2 = gcnew cli::array<int>(100);
   ::array<int> ^ MyArray3 = gcnew ::array<int>(100);
}
```

## <a name="see-also"></a>참고 항목

[.NET 및 UWP용 구성 요소 확장](../windows/component-extensions-for-runtime-platforms.md)