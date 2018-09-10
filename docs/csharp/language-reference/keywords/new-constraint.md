---
title: new, contrainte (référence C#)
ms.date: 07/20/2015
helpviewer_keywords:
- new constraint keyword [C#]
ms.assetid: 58850b64-cb97-4136-be50-1f3bc7fc1da9
ms.openlocfilehash: 9948fc65030a4636c5d23db4ef8c3a584018d2f5
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44087009"
---
# <a name="new-constraint-c-reference"></a><span data-ttu-id="b1702-102">new, contrainte (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b1702-102">new constraint (C# Reference)</span></span>

<span data-ttu-id="b1702-103">La contrainte `new` spécifie que tout argument de type dans une déclaration de classe générique doit avoir un constructeur sans paramètre public.</span><span class="sxs-lookup"><span data-stu-id="b1702-103">The `new` constraint specifies that any type argument in a generic class declaration must have a public parameterless constructor.</span></span> <span data-ttu-id="b1702-104">Pour utiliser la contrainte new, le type ne doit pas être abstract.</span><span class="sxs-lookup"><span data-stu-id="b1702-104">To use the new constraint, the type cannot be abstract.</span></span>

## <a name="example"></a><span data-ttu-id="b1702-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="b1702-105">Example</span></span>

<span data-ttu-id="b1702-106">Appliquez la contrainte `new` à un paramètre de type quand votre classe générique crée des instances du type, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b1702-106">Apply the `new` constraint to a type parameter when your generic class creates new instances of the type, as shown in the following example:</span></span>

[!code-csharp[csrefKeywordsOperator#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#5)]

## <a name="example"></a><span data-ttu-id="b1702-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="b1702-107">Example</span></span>

<span data-ttu-id="b1702-108">Si vous utilisez la contrainte `new()` avec d’autres contraintes, spécifiez-la en dernier :</span><span class="sxs-lookup"><span data-stu-id="b1702-108">When you use the `new()` constraint with other constraints, it must be specified last:</span></span>

[!code-csharp[csrefKeywordsOperator#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#6)]

<span data-ttu-id="b1702-109">Pour plus d’informations, consultez [Contraintes sur les paramètres de type](../../programming-guide/generics/constraints-on-type-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b1702-109">For more information, see [Constraints on Type Parameters](../../programming-guide/generics/constraints-on-type-parameters.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b1702-110">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="b1702-110">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="b1702-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1702-111">See also</span></span>

- <xref:System.Collections.Generic>
- [<span data-ttu-id="b1702-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b1702-112">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="b1702-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b1702-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b1702-114">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="b1702-114">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="b1702-115">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="b1702-115">Operator Keywords</span></span>](operator-keywords.md)
- [<span data-ttu-id="b1702-116">Génériques</span><span class="sxs-lookup"><span data-stu-id="b1702-116">Generics</span></span>](../../programming-guide/generics/index.md)