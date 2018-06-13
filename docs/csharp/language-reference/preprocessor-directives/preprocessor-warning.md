---
title: '#warning (informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '#warning'
helpviewer_keywords:
- '#warning directive [C#]'
ms.assetid: e6fb496d-bb8b-4018-baf6-5b60a0c8902b
ms.openlocfilehash: c56458e0100c23450655e48b2abfb346e18e0bb8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33268181"
---
# <a name="warning-c-reference"></a><span data-ttu-id="2bc3d-102">#warning (référence C#)</span><span class="sxs-lookup"><span data-stu-id="2bc3d-102">#warning (C# Reference)</span></span>
<span data-ttu-id="2bc3d-103">`#warning` vous permet de générer un avertissement de premier niveau à partir d’un emplacement spécifique dans votre code.</span><span class="sxs-lookup"><span data-stu-id="2bc3d-103">`#warning` lets you generate a level one warning from a specific location in your code.</span></span> <span data-ttu-id="2bc3d-104">Exemple :</span><span class="sxs-lookup"><span data-stu-id="2bc3d-104">For example:</span></span>  
  
```csharp
#warning Deprecated code in this method.  
```  
  
## <a name="remarks"></a><span data-ttu-id="2bc3d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="2bc3d-105">Remarks</span></span>  
 <span data-ttu-id="2bc3d-106">`#warning` est souvent utilisé dans une directive conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="2bc3d-106">A common use of `#warning` is in a conditional directive.</span></span> <span data-ttu-id="2bc3d-107">Il est aussi possible de générer une erreur définie par l’utilisateur avec [#error](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md).</span><span class="sxs-lookup"><span data-stu-id="2bc3d-107">It is also possible to generate a user-defined error with [#error](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2bc3d-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="2bc3d-108">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="2bc3d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bc3d-109">See Also</span></span>  
 [<span data-ttu-id="2bc3d-110">Référence C#</span><span class="sxs-lookup"><span data-stu-id="2bc3d-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="2bc3d-111">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2bc3d-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="2bc3d-112">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="2bc3d-112">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
