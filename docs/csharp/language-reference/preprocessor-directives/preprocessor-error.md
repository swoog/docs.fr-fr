---
title: '#error (informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '#error'
helpviewer_keywords:
- '#error directive [C#]'
ms.assetid: f2a7f3af-4cf9-4111-b369-70204d24b26b
ms.openlocfilehash: 9ea4c24dcc3c0a4d39499bee5900cb9c6cc768c9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33269397"
---
# <a name="error-c-reference"></a><span data-ttu-id="ea2cb-102">#error (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ea2cb-102">#error (C# Reference)</span></span>
<span data-ttu-id="ea2cb-103">`#error` vous permet de générer une erreur à partir d’un emplacement spécifique dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ea2cb-103">`#error` lets you generate an error from a specific location in your code.</span></span> <span data-ttu-id="ea2cb-104">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ea2cb-104">For example:</span></span>  
  
```csharp
#error Deprecated code in this method.  
```  
  
## <a name="remarks"></a><span data-ttu-id="ea2cb-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ea2cb-105">Remarks</span></span>  
 <span data-ttu-id="ea2cb-106">`#error` est souvent utilisé dans une directive conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="ea2cb-106">A common use of `#error` is in a conditional directive.</span></span>  
  
 <span data-ttu-id="ea2cb-107">Il est possible aussi de générer un avertissement défini par l’utilisateur avec [#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md).</span><span class="sxs-lookup"><span data-stu-id="ea2cb-107">It is also possible to generate a user-defined warning with [#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ea2cb-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ea2cb-108">Example</span></span>  
  
```csharp
// preprocessor_error.cs  
// CS1029 expected  
#define DEBUG  
class MainClass   
{  
    static void Main()   
    {  
#if DEBUG  
#error DEBUG is defined  
#endif  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="ea2cb-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea2cb-109">See Also</span></span>  
 [<span data-ttu-id="ea2cb-110">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ea2cb-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="ea2cb-111">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ea2cb-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="ea2cb-112">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="ea2cb-112">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
