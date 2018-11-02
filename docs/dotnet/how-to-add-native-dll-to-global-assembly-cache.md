---
title: '방법: 전역 어셈블리 캐시에 네이티브 DLL 추가'
ms.custom: get-started-article
ms.date: 11/04/2016
helpviewer_keywords:
- DLLs [C++], native
- GAC (global assembly cache), loading native DLLs
- native DLLs [C++]
ms.assetid: 25e8d78a-b197-4269-b4e9-237a544ab3c8
ms.openlocfilehash: 1b11ebfae704ca1529113a00b463df728c85fe60
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50641365"
---
# <a name="how-to-add-native-dll-to-global-assembly-cache"></a>방법: 전역 어셈블리 캐시에 네이티브 DLL 추가

COM이 아닌 네이티브 DLL을 전역 어셈블리 캐시에 넣을 수 있습니다.

## <a name="example"></a>예제

**/ASSEMBLYLINKRESOURCE** 네이티브 DLL을 어셈블리에 포함할 수 있습니다.

자세한 내용은 [/ASSEMBLYLINKRESOURCE(.NET Framework 리소스에 대한 링크)](../build/reference/assemblylinkresource-link-to-dotnet-framework-resource.md)를 참조하세요.

```
/ASSEMBLYLINKRESOURCE:MyComponent.dll
```

## <a name="see-also"></a>참고 항목

[C++ Interop 사용(암시적 PInvoke)](../dotnet/using-cpp-interop-implicit-pinvoke.md)