---
title: Fonctions externes (F#)
description: 'Obtenir des informations sur la prise en charge de langage F # pour appeler des fonctions dans le code natif.'
ms.date: 05/16/2016
ms.openlocfilehash: 398697c5e0deab7f8d81ec5198ab1918bd865e13
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="external-functions"></a>Fonctions externes

Cette rubrique décrit F # prise en charge linguistique pour appeler des fonctions dans le code natif.

## <a name="syntax"></a>Syntaxe

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a>Notes

Dans la syntaxe précédente, *arguments* représente les arguments fournis à la `System.Runtime.InteropServices.DllImportAttribute` attribut. Le premier argument est une chaîne qui représente le nom de la DLL qui contient cette fonction, sans l’extension .dll. Arguments supplémentaires peuvent être fournis pour une des propriétés publiques de la `System.Runtime.InteropServices.DllImportAttribute` (classe), telles que la convention d’appel.

Vous possédez une DLL C++ qui contient la fonction exportée suivante natif.

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

Vous pouvez appeler cette fonction à partir de F # en utilisant le code suivant.

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

Interopérabilité avec du code natif est appelée *non managé* et est une fonctionnalité du CLR. Pour plus d’informations, consultez [Interopération avec du code non managé](../../../../docs/framework/interop/index.md). Les informations contenues dans cette section sont applique à F #.


## <a name="see-also"></a>Voir aussi

[Fonctions](index.md)
