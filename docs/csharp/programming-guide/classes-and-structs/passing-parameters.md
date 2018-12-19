---
title: Passage de paramètres - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- parameters [C#], passing
- passing parameters [C#]
- arguments [C#]
- methods [C#], passing parameters
- C# language, method parameters
ms.assetid: a5c3003f-7441-4710-b8b1-c79de77e0b77
ms.openlocfilehash: 3e205ecba48df69c0e7f289ad8201765b35d5767
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53238141"
---
# <a name="passing-parameters-c-programming-guide"></a><span data-ttu-id="78cdf-102">Passage de paramètres (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="78cdf-102">Passing Parameters (C# Programming Guide)</span></span>
<span data-ttu-id="78cdf-103">En C#, les arguments peuvent être passés aux paramètres par valeur ou par référence.</span><span class="sxs-lookup"><span data-stu-id="78cdf-103">In C#, arguments can be passed to parameters either by value or by reference.</span></span> <span data-ttu-id="78cdf-104">Avec le passage par référence, les fonctions membres, les méthodes, les propriétés, les indexeurs, les opérateurs et les constructeurs peuvent changer la valeur des paramètres et rendre cette modification persistante dans l’environnement d’appel.</span><span class="sxs-lookup"><span data-stu-id="78cdf-104">Passing by reference enables function members, methods, properties, indexers, operators, and constructors to change the value of the parameters and have that change persist in the calling environment.</span></span> <span data-ttu-id="78cdf-105">Pour passer un paramètre par référence avec l’intention de changer la valeur, utilisez le mot clé `ref` ou `out`.</span><span class="sxs-lookup"><span data-stu-id="78cdf-105">To pass a parameter by reference with the intent of changing the value, use the `ref`, or `out` keyword.</span></span> <span data-ttu-id="78cdf-106">Pour passer un paramètre par référence avec l’intention d’éviter la copie, mais de ne pas changer la valeur, utilisez le modificateur `in`.</span><span class="sxs-lookup"><span data-stu-id="78cdf-106">To pass by reference with the intent of avoiding copying but not changing the value, use the `in` modifier.</span></span> <span data-ttu-id="78cdf-107">Pour plus de simplicité, les exemples de cette rubrique utilisent uniquement le mot clé `ref`.</span><span class="sxs-lookup"><span data-stu-id="78cdf-107">For simplicity, only the `ref` keyword is used in the examples in this topic.</span></span> <span data-ttu-id="78cdf-108">Pour plus d’informations sur la différence entre `in`, `ref` et `out`, consultez [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md) et [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md).</span><span class="sxs-lookup"><span data-stu-id="78cdf-108">For more information about the difference between `in`, `ref`, and `out`, see [in](../../../csharp/language-reference/keywords/in-parameter-modifier.md), [ref](../../../csharp/language-reference/keywords/ref.md), and [out](../../../csharp/language-reference/keywords/out-parameter-modifier.md).</span></span>  
  
 <span data-ttu-id="78cdf-109">L’exemple suivant illustre la différence entre les paramètres de référence et de valeur.</span><span class="sxs-lookup"><span data-stu-id="78cdf-109">The following example illustrates the difference between value and reference parameters.</span></span>  
  
 [!code-csharp[csProgGuideParameters#10](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/passing-parameters_1.cs)]  
  
 <span data-ttu-id="78cdf-110">Pour plus d’informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="78cdf-110">For more information, see the following topics:</span></span>  
  
-   [<span data-ttu-id="78cdf-111">Passage de paramètres de type valeur</span><span class="sxs-lookup"><span data-stu-id="78cdf-111">Passing Value-Type Parameters</span></span>](../../../csharp/programming-guide/classes-and-structs/passing-value-type-parameters.md)  
  
-   [<span data-ttu-id="78cdf-112">Passage de paramètres de type référence</span><span class="sxs-lookup"><span data-stu-id="78cdf-112">Passing Reference-Type Parameters</span></span>](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="78cdf-113">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="78cdf-113">C# Language Specification</span></span>  

<span data-ttu-id="78cdf-114">Pour plus d’informations, consultez [Liste des arguments](~/_csharplang/spec/expressions.md#argument-lists) dans la [Spécification du langage C#](../../language-reference/language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="78cdf-114">For more information, see [Argument lists](~/_csharplang/spec/expressions.md#argument-lists) in the [C# Language Specification](../../language-reference/language-specification/index.md).</span></span> <span data-ttu-id="78cdf-115">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="78cdf-115">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78cdf-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78cdf-116">See Also</span></span>

- [<span data-ttu-id="78cdf-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="78cdf-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="78cdf-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="78cdf-118">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)
