---
title: '#warning (informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '#warning'
helpviewer_keywords:
- '#warning directive [C#]'
ms.assetid: e6fb496d-bb8b-4018-baf6-5b60a0c8902b
ms.openlocfilehash: 59ca63d5089e377627a9116f24f9a0a1681bb4b2
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932675"
---
# <a name="warning-c-reference"></a><span data-ttu-id="eaf38-102">#warning (référence C#)</span><span class="sxs-lookup"><span data-stu-id="eaf38-102">#warning (C# Reference)</span></span>
<span data-ttu-id="eaf38-103">`#warning` vous permet de générer un avertissement du compilateur de premier niveau [CS1030](../../misc/cs1030.md) à partir d’un emplacement spécifique dans votre code.</span><span class="sxs-lookup"><span data-stu-id="eaf38-103">`#warning` lets you generate a [CS1030](../../misc/cs1030.md) level one compiler warning from a specific location in your code.</span></span> <span data-ttu-id="eaf38-104">Exemple :</span><span class="sxs-lookup"><span data-stu-id="eaf38-104">For example:</span></span>  
  
```csharp
#warning Deprecated code in this method.  
```  
  
## <a name="remarks"></a><span data-ttu-id="eaf38-105">Notes</span><span class="sxs-lookup"><span data-stu-id="eaf38-105">Remarks</span></span>
 <span data-ttu-id="eaf38-106">`#warning` est souvent utilisé dans une directive conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="eaf38-106">A common use of `#warning` is in a conditional directive.</span></span> <span data-ttu-id="eaf38-107">Il est aussi possible de générer une erreur définie par l’utilisateur avec [#error](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md).</span><span class="sxs-lookup"><span data-stu-id="eaf38-107">It is also possible to generate a user-defined error with [#error](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="eaf38-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="eaf38-108">Example</span></span>  

```csharp
// preprocessor_warning.cs  
// CS1030 expected  
#define DEBUG  
class MainClass
{  
    static void Main()
    {  
#if DEBUG  
#warning DEBUG is defined  
#endif  
    }  
}  
```  

## <a name="see-also"></a><span data-ttu-id="eaf38-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf38-109">See Also</span></span>

- [<span data-ttu-id="eaf38-110">Référence C#</span><span class="sxs-lookup"><span data-stu-id="eaf38-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="eaf38-111">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="eaf38-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="eaf38-112">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="eaf38-112">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
