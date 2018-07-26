---
title: new, contrainte (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- new constraint keyword [C#]
ms.assetid: 58850b64-cb97-4136-be50-1f3bc7fc1da9
ms.openlocfilehash: 77c955102ba9cede831c85838a6a7e57025ad35b
ms.sourcegitcommit: 2d8b7488d94101b534ca3e9780b1c1e840233405
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2018
ms.locfileid: "39199458"
---
# <a name="new-constraint-c-reference"></a><span data-ttu-id="794bc-102">new, contrainte (référence C#)</span><span class="sxs-lookup"><span data-stu-id="794bc-102">new Constraint (C# Reference)</span></span>
<span data-ttu-id="794bc-103">La contrainte `new` spécifie que tout argument de type dans une déclaration de classe générique doit avoir un constructeur sans paramètre public.</span><span class="sxs-lookup"><span data-stu-id="794bc-103">The `new` constraint specifies that any type argument in a generic class declaration must have a public parameterless constructor.</span></span> <span data-ttu-id="794bc-104">Pour utiliser la contrainte new, le type ne doit pas être abstract.</span><span class="sxs-lookup"><span data-stu-id="794bc-104">To use the new constraint, the type cannot be abstract.</span></span>  
  
## <a name="example"></a><span data-ttu-id="794bc-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="794bc-105">Example</span></span>  
 <span data-ttu-id="794bc-106">Appliquez la contrainte `new` à un paramètre de type quand votre classe générique crée des instances du type, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="794bc-106">Apply the `new` constraint to a type parameter when your generic class creates new instances of the type, as shown in the following example:</span></span>  
  
 [!code-csharp[csrefKeywordsOperator#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/new-constraint_1.cs)]  
  
## <a name="example"></a><span data-ttu-id="794bc-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="794bc-107">Example</span></span>  
 <span data-ttu-id="794bc-108">Si vous utilisez la contrainte `new()` avec d’autres contraintes, spécifiez-la en dernier :</span><span class="sxs-lookup"><span data-stu-id="794bc-108">When you use the `new()` constraint with other constraints, it must be specified last:</span></span>  
  
 [!code-csharp[csrefKeywordsOperator#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/new-constraint_2.cs)]  
  
 <span data-ttu-id="794bc-109">Pour plus d’informations, consultez [Contraintes sur les paramètres de type](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="794bc-109">For more information, see [Constraints on Type Parameters](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="794bc-110">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="794bc-110">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="794bc-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="794bc-111">See Also</span></span>  
 <xref:System.Collections.Generic>  
 [<span data-ttu-id="794bc-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="794bc-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="794bc-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="794bc-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="794bc-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="794bc-114">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="794bc-115">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="794bc-115">Operator Keywords</span></span>](../../../csharp/language-reference/keywords/operator-keywords.md)  
 [<span data-ttu-id="794bc-116">Génériques</span><span class="sxs-lookup"><span data-stu-id="794bc-116">Generics</span></span>](../../../csharp/programming-guide/generics/index.md)
