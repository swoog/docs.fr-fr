---
title: implicit - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- implicit
- implicit_CSharpKeyword
helpviewer_keywords:
- implicit keyword [C#]
ms.assetid: 34db590e-eb3a-4f11-88d0-ffb3cd753dab
ms.openlocfilehash: ee40db31aeb39a37c6ab15b26b48f1f7d02d6780
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240578"
---
# <a name="implicit-c-reference"></a><span data-ttu-id="e3432-102">implicit (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e3432-102">implicit (C# Reference)</span></span>

<span data-ttu-id="e3432-103">Le mot clé `implicit` est utilisé pour déclarer un opérateur de conversion de type implicite défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3432-103">The `implicit` keyword is used to declare an implicit user-defined type conversion operator.</span></span> <span data-ttu-id="e3432-104">Utilisez-le pour permettre les conversions implicites entre un type défini par l’utilisateur et un autre type, si la conversion n’est pas susceptible de provoquer une perte de données.</span><span class="sxs-lookup"><span data-stu-id="e3432-104">Use it to enable implicit conversions between a user-defined type and another type, if the conversion is guaranteed not to cause a loss of data.</span></span>

## <a name="example"></a><span data-ttu-id="e3432-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="e3432-105">Example</span></span>

[!code-csharp[csrefKeywordsConversion#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#5)]

<span data-ttu-id="e3432-106">En éliminant les casts de type superflus, les conversions implicites peuvent améliorer la lisibilité du code source.</span><span class="sxs-lookup"><span data-stu-id="e3432-106">By eliminating unnecessary casts, implicit conversions can improve source code readability.</span></span> <span data-ttu-id="e3432-107">Toutefois, étant donné que les conversions implicites ne nécessitent pas que les programmeurs castent explicitement d’un type à un autre, il faut veiller à éviter les résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="e3432-107">However, because implicit conversions do not require programmers to explicitly cast from one type to the other, care must be taken to prevent unexpected results.</span></span> <span data-ttu-id="e3432-108">En général, les opérateurs de conversion implicite ne doivent jamais lever d’exceptions ni perdre d’informations pour pouvoir être utilisés en toute sécurité à l’insu du programmeur.</span><span class="sxs-lookup"><span data-stu-id="e3432-108">In general, implicit conversion operators should never throw exceptions and never lose information so that they can be used safely without the programmer's awareness.</span></span> <span data-ttu-id="e3432-109">Si un opérateur de conversion ne peut pas répondre à ces critères, il doit être marqué comme `explicit`.</span><span class="sxs-lookup"><span data-stu-id="e3432-109">If a conversion operator cannot meet those criteria, it should be marked `explicit`.</span></span> <span data-ttu-id="e3432-110">Pour plus d’informations, consultez [Utilisation d’opérateurs de conversion](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).</span><span class="sxs-lookup"><span data-stu-id="e3432-110">For more information, see [Using Conversion Operators](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="e3432-111">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="e3432-111">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="e3432-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3432-112">See also</span></span>

- [<span data-ttu-id="e3432-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e3432-113">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="e3432-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e3432-114">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="e3432-115">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="e3432-115">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="e3432-116">explicit</span><span class="sxs-lookup"><span data-stu-id="e3432-116">explicit</span></span>](explicit.md)  
- [<span data-ttu-id="e3432-117">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e3432-117">operator (C# Reference)</span></span>](operator.md)  
- [<span data-ttu-id="e3432-118">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="e3432-118">How to: Implement User-Defined Conversions Between Structs</span></span>](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
