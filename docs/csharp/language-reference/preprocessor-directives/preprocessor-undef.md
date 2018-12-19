---
title: '#undef - Référence sur C#'
ms.custom: seodec18
ms.date: 06/30/2018
f1_keywords:
- '#undef'
helpviewer_keywords:
- '#undef directive [C#]'
ms.assetid: 686c92d2-7194-4be4-b2f4-80091712d513
ms.openlocfilehash: 5a3658c4e6bb32158e6f81c3ac5014fbedba0713
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235758"
---
# <a name="undef-c-reference"></a><span data-ttu-id="2c0d7-102">#undef (référence C#)</span><span class="sxs-lookup"><span data-stu-id="2c0d7-102">#undef (C# Reference)</span></span>
<span data-ttu-id="2c0d7-103">`#undef` vous permet d’annuler la définition d’un symbole de telle sorte qu’en utilisant le symbole comme expression dans une directive [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md), l’expression correspond à `false`.</span><span class="sxs-lookup"><span data-stu-id="2c0d7-103">`#undef` lets you undefine a symbol, such that, by using the symbol as the expression in a [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive, the expression will evaluate to `false`.</span></span>  
  
 <span data-ttu-id="2c0d7-104">Un symbole peut être défini avec la directive [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) ou l’option du compilateur [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="2c0d7-104">A symbol can be defined either with the [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) directive or the [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md) compiler option.</span></span> <span data-ttu-id="2c0d7-105">La directive `#undef` doit figurer dans le fichier préalablement à l’utilisation d’instructions qui ne sont pas aussi des directives.</span><span class="sxs-lookup"><span data-stu-id="2c0d7-105">The `#undef` directive must appear in the file before you use any statements that are not also directives.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c0d7-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="2c0d7-106">Example</span></span>  

```csharp
// preprocessor_undef.cs  
// compile with: /d:DEBUG  
#undef DEBUG  
using System;  
class MyClass
{  
    static void Main()
    {  
#if DEBUG  
        Console.WriteLine("DEBUG is defined");  
#else  
        Console.WriteLine("DEBUG is not defined");  
#endif  
    }  
}  
```

<span data-ttu-id="2c0d7-107">**DEBUG n’est pas défini**</span><span class="sxs-lookup"><span data-stu-id="2c0d7-107">**DEBUG is not defined**</span></span>

## <a name="see-also"></a><span data-ttu-id="2c0d7-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c0d7-108">See Also</span></span>

- [<span data-ttu-id="2c0d7-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="2c0d7-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="2c0d7-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2c0d7-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2c0d7-111">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="2c0d7-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
