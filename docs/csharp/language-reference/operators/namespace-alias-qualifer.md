---
title: ':: Opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 2e456be075f3487676228244e0119ff46ed9a538
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243476"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="58616-102">:: Opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="58616-102">:: Operator (C# Reference)</span></span>
<span data-ttu-id="58616-103">Le qualificateur d’alias d’espace de noms (`::`) s’utilise pour rechercher les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="58616-103">The namespace alias qualifier (`::`) is used to look up identifiers.</span></span> <span data-ttu-id="58616-104">Il se place toujours entre deux identificateurs, comme dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="58616-104">It is always positioned between two identifiers, as in this example:</span></span>  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  

<span data-ttu-id="58616-105">L’opérateur `::` peut également être utilisé avec une *directive d’alias using* :</span><span class="sxs-lookup"><span data-stu-id="58616-105">The `::` operator can also be used with a *using alias directive*:</span></span>

```csharp
// using Col=System.Collections.Generic;
var numbers = new Col::List<int> { 1, 2, 3 };
```

## <a name="remarks"></a><span data-ttu-id="58616-106">Notes</span><span class="sxs-lookup"><span data-stu-id="58616-106">Remarks</span></span>  
 <span data-ttu-id="58616-107">Le qualificateur d’alias d’espace de noms peut être `global`.</span><span class="sxs-lookup"><span data-stu-id="58616-107">The namespace alias qualifier can be `global`.</span></span> <span data-ttu-id="58616-108">Il appelle alors une recherche dans l’espace de noms global, plutôt que dans un espace de noms avec alias.</span><span class="sxs-lookup"><span data-stu-id="58616-108">This invokes a lookup in the global namespace, rather than an aliased namespace.</span></span>  
  
## <a name="for-more-information"></a><span data-ttu-id="58616-109">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="58616-109">For More Information</span></span>  
 <span data-ttu-id="58616-110">Pour obtenir un exemple d’utilisation de l’opérateur `::`, consultez la section suivante :</span><span class="sxs-lookup"><span data-stu-id="58616-110">For an example of how to use the `::` operator, see the following section:</span></span>  
  
-   [<span data-ttu-id="58616-111">Guide pratique pour utiliser l’alias d’espace de noms global</span><span class="sxs-lookup"><span data-stu-id="58616-111">How to: Use the Global Namespace Alias</span></span>](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="58616-112">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="58616-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="58616-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58616-113">See Also</span></span>

- [<span data-ttu-id="58616-114">Référence C#</span><span class="sxs-lookup"><span data-stu-id="58616-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="58616-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="58616-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="58616-116">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="58616-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="58616-117">Mots clés d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="58616-117">Namespace Keywords</span></span>](../../../csharp/language-reference/keywords/namespace-keywords.md)  
- [<span data-ttu-id="58616-118">. Opérateur</span><span class="sxs-lookup"><span data-stu-id="58616-118">. Operator</span></span>](../../../csharp/language-reference/operators/member-access-operator.md)  
- [<span data-ttu-id="58616-119">extern alias</span><span class="sxs-lookup"><span data-stu-id="58616-119">extern alias</span></span>](../../../csharp/language-reference/keywords/extern-alias.md)
