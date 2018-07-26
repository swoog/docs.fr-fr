---
title: operator (référence C#)
ms.date: 07/20/2015
f1_keywords:
- operator_CSharpKeyword
- operator
helpviewer_keywords:
- operator keyword [C#]
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
ms.openlocfilehash: d633a46e21f913aa8c05289dccfb63e71efd697e
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37959542"
---
# <a name="operator-c-reference"></a><span data-ttu-id="4b76b-102">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4b76b-102">operator (C# Reference)</span></span>
<span data-ttu-id="4b76b-103">Utilisez le mot clé `operator` pour surcharger un opérateur intégré ou pour fournir une conversion définie par l’utilisateur dans une déclaration class ou struct.</span><span class="sxs-lookup"><span data-stu-id="4b76b-103">Use the `operator` keyword to overload a built-in operator or to provide a user-defined conversion in a class or struct declaration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b76b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b76b-104">Example</span></span>  
 <span data-ttu-id="4b76b-105">L’exemple suivant montre une classe très simplifiée pour les nombres fractionnaires.</span><span class="sxs-lookup"><span data-stu-id="4b76b-105">The following is a very simplified class for fractional numbers.</span></span> <span data-ttu-id="4b76b-106">Cette classe surcharge les opérateurs `+` et `*` pour effectuer des opérations d’addition et de multiplication fractionnaires. Elle fournit également un opérateur de conversion qui convertit un type `Fraction` en type `double`.</span><span class="sxs-lookup"><span data-stu-id="4b76b-106">It overloads the `+` and `*` operators to perform fractional addition and multiplication, and also provides a conversion operator that converts a `Fraction` type to a `double` type.</span></span>  
  
 [!code-csharp[csrefKeywordsConversion#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/operator_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="4b76b-107">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="4b76b-107">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4b76b-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b76b-108">See Also</span></span>  
 [<span data-ttu-id="4b76b-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4b76b-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="4b76b-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4b76b-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="4b76b-111">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="4b76b-111">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="4b76b-112">implicit</span><span class="sxs-lookup"><span data-stu-id="4b76b-112">implicit</span></span>](../../../csharp/language-reference/keywords/implicit.md)  
 [<span data-ttu-id="4b76b-113">explicit</span><span class="sxs-lookup"><span data-stu-id="4b76b-113">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)  
 [<span data-ttu-id="4b76b-114">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="4b76b-114">How to: Implement User-Defined Conversions Between Structs</span></span>](../../../csharp/programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
