---
title: unchecked, mot clé - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- unchecked_CSharpKeyword
- unchecked
helpviewer_keywords:
- unchecked keyword [C#]
ms.assetid: 0c021f7c-923f-4b3d-a58f-55336f5ac27e
ms.openlocfilehash: 0d96b9af0eaee81da8532c1facbfa8b1d1a8128f
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633496"
---
# <a name="unchecked-c-reference"></a><span data-ttu-id="a2287-102">unchecked (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a2287-102">unchecked (C# Reference)</span></span>

<span data-ttu-id="a2287-103">Le mot clé `unchecked` permet de supprimer le contrôle de dépassement de capacité pour les conversions et les opérations arithmétiques de type intégral.</span><span class="sxs-lookup"><span data-stu-id="a2287-103">The `unchecked` keyword is used to suppress overflow-checking for integral-type arithmetic operations and conversions.</span></span>

<span data-ttu-id="a2287-104">Dans un contexte non vérifié (unchecked), si une expression produit une valeur située hors de la plage du type de destination, le dépassement de capacité n’est pas signalé.</span><span class="sxs-lookup"><span data-stu-id="a2287-104">In an unchecked context, if an expression produces a value that is outside the range of the destination type, the overflow is not flagged.</span></span> <span data-ttu-id="a2287-105">Par exemple, comme le calcul dans l’exemple suivant s’effectue dans un bloc ou une expression `unchecked`, le fait que le résultat est trop grand pour un entier est ignoré et `int1` se voit assigner la valeur -2,147,483,639.</span><span class="sxs-lookup"><span data-stu-id="a2287-105">For example, because the calculation in the following example is performed in an `unchecked` block or expression, the fact that the result is too large for an integer is ignored, and `int1` is assigned the value -2,147,483,639.</span></span>

[!code-csharp[csrefKeywordsChecked#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsChecked/CS/csrefKeywordsChecked.cs#5)]

<span data-ttu-id="a2287-106">Si l’environnement `unchecked` est supprimé, une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="a2287-106">If the `unchecked` environment is removed, a compilation error occurs.</span></span> <span data-ttu-id="a2287-107">Le dépassement de capacité peut être détecté au moment de la compilation, car tous les termes de l’expression sont des constantes.</span><span class="sxs-lookup"><span data-stu-id="a2287-107">The overflow can be detected at compile time because all the terms of the expression are constants.</span></span>

<span data-ttu-id="a2287-108">Les expressions qui contiennent des termes non constants sont non vérifiées par défaut au moment de la compilation et de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a2287-108">Expressions that contain non-constant terms are unchecked by default at compile time and run time.</span></span> <span data-ttu-id="a2287-109">Consultez [checked](checked.md) pour plus d’informations sur l’activation d’un environnement vérifié (checked).</span><span class="sxs-lookup"><span data-stu-id="a2287-109">See [checked](checked.md) for information about enabling a checked environment.</span></span>

<span data-ttu-id="a2287-110">Étant donné que la vérification de dépassement de capacité prend du temps, l’utilisation de code non vérifié dans les situations où il n’existe aucun danger de dépassement de capacité peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="a2287-110">Because checking for overflow takes time, the use of unchecked code in situations where there is no danger of overflow might improve performance.</span></span> <span data-ttu-id="a2287-111">Toutefois, si un dépassement de capacité est possible, il convient d’utiliser un environnement vérifié (checked).</span><span class="sxs-lookup"><span data-stu-id="a2287-111">However, if overflow is a possibility, a checked environment should be used.</span></span>

## <a name="example"></a><span data-ttu-id="a2287-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2287-112">Example</span></span>

<span data-ttu-id="a2287-113">L’exemple de code suivant montre comment utiliser le mot clé `unchecked`.</span><span class="sxs-lookup"><span data-stu-id="a2287-113">This sample shows how to use the `unchecked` keyword.</span></span>

[!code-csharp[csrefKeywordsChecked#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsChecked/CS/csrefKeywordsChecked.cs#2)]

## <a name="c-language-specification"></a><span data-ttu-id="a2287-114">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="a2287-114">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="a2287-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2287-115">See also</span></span>

- [<span data-ttu-id="a2287-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a2287-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="a2287-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a2287-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="a2287-118">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="a2287-118">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="a2287-119">Checked et unchecked</span><span class="sxs-lookup"><span data-stu-id="a2287-119">Checked and Unchecked</span></span>](checked-and-unchecked.md)
- [<span data-ttu-id="a2287-120">checked</span><span class="sxs-lookup"><span data-stu-id="a2287-120">checked</span></span>](checked.md)
