---
title: implicit (référence C#)
ms.date: 07/20/2015
f1_keywords:
- implicit
- implicit_CSharpKeyword
helpviewer_keywords:
- implicit keyword [C#]
ms.assetid: 34db590e-eb3a-4f11-88d0-ffb3cd753dab
ms.openlocfilehash: 70379136fd4b14403eac919ac15590250b17b416
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44273247"
---
# <a name="implicit-c-reference"></a><span data-ttu-id="ec859-102">implicit (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ec859-102">implicit (C# Reference)</span></span>

<span data-ttu-id="ec859-103">Le mot clé `implicit` est utilisé pour déclarer un opérateur de conversion de type implicite défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ec859-103">The `implicit` keyword is used to declare an implicit user-defined type conversion operator.</span></span> <span data-ttu-id="ec859-104">Utilisez-le pour permettre les conversions implicites entre un type défini par l’utilisateur et un autre type, si la conversion n’est pas susceptible de provoquer une perte de données.</span><span class="sxs-lookup"><span data-stu-id="ec859-104">Use it to enable implicit conversions between a user-defined type and another type, if the conversion is guaranteed not to cause a loss of data.</span></span>

## <a name="example"></a><span data-ttu-id="ec859-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec859-105">Example</span></span>

[!code-csharp[csrefKeywordsConversion#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsConversion/CS/csrefKeywordsConversion.cs#5)]

<span data-ttu-id="ec859-106">En éliminant les casts de type superflus, les conversions implicites peuvent améliorer la lisibilité du code source.</span><span class="sxs-lookup"><span data-stu-id="ec859-106">By eliminating unnecessary casts, implicit conversions can improve source code readability.</span></span> <span data-ttu-id="ec859-107">Toutefois, étant donné que les conversions implicites ne nécessitent pas que les programmeurs castent explicitement d’un type à un autre, il faut veiller à éviter les résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="ec859-107">However, because implicit conversions do not require programmers to explicitly cast from one type to the other, care must be taken to prevent unexpected results.</span></span> <span data-ttu-id="ec859-108">En général, les opérateurs de conversion implicite ne doivent jamais lever d’exceptions ni perdre d’informations pour pouvoir être utilisés en toute sécurité à l’insu du programmeur.</span><span class="sxs-lookup"><span data-stu-id="ec859-108">In general, implicit conversion operators should never throw exceptions and never lose information so that they can be used safely without the programmer's awareness.</span></span> <span data-ttu-id="ec859-109">Si un opérateur de conversion ne peut pas répondre à ces critères, il doit être marqué comme `explicit`.</span><span class="sxs-lookup"><span data-stu-id="ec859-109">If a conversion operator cannot meet those criteria, it should be marked `explicit`.</span></span> <span data-ttu-id="ec859-110">Pour plus d’informations, consultez [Utilisation d’opérateurs de conversion](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).</span><span class="sxs-lookup"><span data-stu-id="ec859-110">For more information, see [Using Conversion Operators](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="ec859-111">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="ec859-111">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="ec859-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec859-112">See also</span></span>

- [<span data-ttu-id="ec859-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ec859-113">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="ec859-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ec859-114">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="ec859-115">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="ec859-115">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="ec859-116">explicit</span><span class="sxs-lookup"><span data-stu-id="ec859-116">explicit</span></span>](explicit.md)  
- [<span data-ttu-id="ec859-117">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ec859-117">operator (C# Reference)</span></span>](operator.md)  
- [<span data-ttu-id="ec859-118">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="ec859-118">How to: Implement User-Defined Conversions Between Structs</span></span>](../../programming-guide/statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)
