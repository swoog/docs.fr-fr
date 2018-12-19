---
title: '#error - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#error'
helpviewer_keywords:
- '#error directive [C#]'
ms.assetid: f2a7f3af-4cf9-4111-b369-70204d24b26b
ms.openlocfilehash: b335dfeed23d43938c66f0753590af55ac99b12a
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235586"
---
# <a name="error-c-reference"></a><span data-ttu-id="ec2c7-102">#error (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ec2c7-102">#error (C# Reference)</span></span>
<span data-ttu-id="ec2c7-103">`#error` vous permet de générer une erreur définie par l’utilisateur [CS1029](../compiler-messages/cs1029.md) à partir d’un emplacement spécifique dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-103">`#error` lets you generate a [CS1029](../compiler-messages/cs1029.md) user-defined error from a specific location in your code.</span></span> <span data-ttu-id="ec2c7-104">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ec2c7-104">For example:</span></span>  
  
```csharp
#error Deprecated code in this method.  
```  
  
## <a name="remarks"></a><span data-ttu-id="ec2c7-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ec2c7-105">Remarks</span></span>  
 <span data-ttu-id="ec2c7-106">`#error` est souvent utilisé dans une directive conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-106">A common use of `#error` is in a conditional directive.</span></span>  
  
 <span data-ttu-id="ec2c7-107">Il est possible aussi de générer un avertissement défini par l’utilisateur avec [#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md).</span><span class="sxs-lookup"><span data-stu-id="ec2c7-107">It is also possible to generate a user-defined warning with [#warning](../../../csharp/language-reference/preprocessor-directives/preprocessor-warning.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec2c7-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec2c7-108">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="ec2c7-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec2c7-109">See Also</span></span>

- [<span data-ttu-id="ec2c7-110">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ec2c7-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="ec2c7-111">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ec2c7-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="ec2c7-112">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="ec2c7-112">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
