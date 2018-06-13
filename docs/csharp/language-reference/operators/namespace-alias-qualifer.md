---
title: ::, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ::_CSharpKeyword
helpviewer_keywords:
- ':: operator [C#]'
- 'namespaces [C#], :: operator'
- namespace alias qualifier operator (::) [C#]
ms.assetid: 698b5a73-85cf-4e0e-9e8e-6496887f8527
ms.openlocfilehash: 668799a2d846d0f0bf1b3743e202602250a57ae5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33271771"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="9114e-102">::, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9114e-102">:: Operator (C# Reference)</span></span>
<span data-ttu-id="9114e-103">Le qualificateur d’alias d’espace de noms (`::`) s’utilise pour rechercher les identificateurs.</span><span class="sxs-lookup"><span data-stu-id="9114e-103">The namespace alias qualifier (`::`) is used to look up identifiers.</span></span> <span data-ttu-id="9114e-104">Il se place toujours entre deux identificateurs, comme dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="9114e-104">It is always positioned between two identifiers, as in this example:</span></span>  
  
 [!code-csharp[csRefOperators#27](../../../csharp/language-reference/operators/codesnippet/CSharp/namespace-alias-qualifer_1.cs)]  
  
## <a name="remarks"></a><span data-ttu-id="9114e-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9114e-105">Remarks</span></span>  
 <span data-ttu-id="9114e-106">Le qualificateur d’alias d’espace de noms peut être `global`.</span><span class="sxs-lookup"><span data-stu-id="9114e-106">The namespace alias qualifier can be `global`.</span></span> <span data-ttu-id="9114e-107">Il appelle alors une recherche dans l’espace de noms global, plutôt que dans un espace de noms avec alias.</span><span class="sxs-lookup"><span data-stu-id="9114e-107">This invokes a lookup in the global namespace, rather than an aliased namespace.</span></span>  
  
## <a name="for-more-information"></a><span data-ttu-id="9114e-108">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="9114e-108">For More Information</span></span>  
 <span data-ttu-id="9114e-109">Pour obtenir un exemple d’utilisation de l’opérateur `::`, consultez la section suivante :</span><span class="sxs-lookup"><span data-stu-id="9114e-109">For an example of how to use the `::` operator, see the following section:</span></span>  
  
-   [<span data-ttu-id="9114e-110">Comment : utiliser l’alias d’espace de noms global</span><span class="sxs-lookup"><span data-stu-id="9114e-110">How to: Use the Global Namespace Alias</span></span>](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="9114e-111">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9114e-111">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9114e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9114e-112">See Also</span></span>  
 [<span data-ttu-id="9114e-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9114e-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="9114e-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9114e-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="9114e-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="9114e-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="9114e-116">Mots clés d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9114e-116">Namespace Keywords</span></span>](../../../csharp/language-reference/keywords/namespace-keywords.md)  
 [<span data-ttu-id="9114e-117">. Opérateur</span><span class="sxs-lookup"><span data-stu-id="9114e-117">. Operator</span></span>](../../../csharp/language-reference/operators/member-access-operator.md)  
 [<span data-ttu-id="9114e-118">extern alias</span><span class="sxs-lookup"><span data-stu-id="9114e-118">extern alias</span></span>](../../../csharp/language-reference/keywords/extern-alias.md)
