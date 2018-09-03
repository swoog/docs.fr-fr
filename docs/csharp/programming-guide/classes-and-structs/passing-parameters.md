---
title: Passage de paramètres (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- parameters [C#], passing
- passing parameters [C#]
- arguments [C#]
- methods [C#], passing parameters
- C# language, method parameters
ms.assetid: a5c3003f-7441-4710-b8b1-c79de77e0b77
ms.openlocfilehash: a1ccfff8081d101eee46360009653b0591dfb3ff
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43404124"
---
# <a name="passing-parameters-c-programming-guide"></a><span data-ttu-id="07629-102">Passage de paramètres (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="07629-102">Passing Parameters (C# Programming Guide)</span></span>
<span data-ttu-id="07629-103">En C#, les arguments peuvent être passés aux paramètres par valeur ou par référence.</span><span class="sxs-lookup"><span data-stu-id="07629-103">In C#, arguments can be passed to parameters either by value or by reference.</span></span> <span data-ttu-id="07629-104">Avec le passage par référence, les fonctions membres, les méthodes, les propriétés, les indexeurs, les opérateurs et les constructeurs peuvent changer la valeur des paramètres et rendre cette modification persistante dans l’environnement d’appel.</span><span class="sxs-lookup"><span data-stu-id="07629-104">Passing by reference enables function members, methods, properties, indexers, operators, and constructors to change the value of the parameters and have that change persist in the calling environment.</span></span> <span data-ttu-id="07629-105">Pour passer un paramètre par référence avec l’intention de changer la valeur, utilisez le mot clé `ref` ou `out`.</span><span class="sxs-lookup"><span data-stu-id="07629-105">To pass a parameter by reference with the intent of changing the value, use the `ref`, or `out` keyword.</span></span> <span data-ttu-id="07629-106">Pour passer un paramètre par référence avec l’intention d’éviter la copie, mais de ne pas changer la valeur, utilisez le modificateur `in`.</span><span class="sxs-lookup"><span data-stu-id="07629-106">To pass by reference with the intent of avoiding copying but not changing the value, use the `in` modifier.</span></span> <span data-ttu-id="07629-107">Pour plus de simplicité, les exemples de cette rubrique utilisent uniquement le mot clé `ref`.</span><span class="sxs-lookup"><span data-stu-id="07629-107">For simplicity, only the `ref` keyword is used in the examples in this topic.</span></span> <span data-ttu-id="07629-108">Pour plus d’informations sur la différence entre `in`, `ref` et `out`, consultez [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md), [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md) et [Passage de tableaux à l’aide de paramètres ref et out](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).</span><span class="sxs-lookup"><span data-stu-id="07629-108">For more information about the difference between `in`, `ref`, and `out`, see [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md), [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md), and [Passing Arrays Using ref and out](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).</span></span>  
  
 <span data-ttu-id="07629-109">L’exemple suivant illustre la différence entre les paramètres de référence et de valeur.</span><span class="sxs-lookup"><span data-stu-id="07629-109">The following example illustrates the difference between value and reference parameters.</span></span>  
  
 [!code-csharp[csProgGuideParameters#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/passing-parameters_1.cs)]  
  
 <span data-ttu-id="07629-110">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="07629-110">For more information, see the following topics:</span></span>  
  
-   [<span data-ttu-id="07629-111">Passage de paramètres de type valeur</span><span class="sxs-lookup"><span data-stu-id="07629-111">Passing Value-Type Parameters</span></span>](../../../csharp/programming-guide/classes-and-structs/passing-value-type-parameters.md)  
  
-   [<span data-ttu-id="07629-112">Passage de paramètres de type référence</span><span class="sxs-lookup"><span data-stu-id="07629-112">Passing Reference-Type Parameters</span></span>](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="07629-113">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="07629-113">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="07629-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07629-114">See Also</span></span>  
 [<span data-ttu-id="07629-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="07629-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="07629-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="07629-116">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)
