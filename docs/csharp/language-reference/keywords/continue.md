---
title: continue, instruction - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- continue_CSharpKeyword
- continue
helpviewer_keywords:
- continue keyword [C#]
ms.assetid: 8a5ac96f-f98a-4519-b32d-345847ed7be0
ms.openlocfilehash: 0b3baf6eb4843ff67a3d76af06ca86ca9ec2db03
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690590"
---
# <a name="continue-c-reference"></a><span data-ttu-id="10fc4-102">continue (référence C#)</span><span class="sxs-lookup"><span data-stu-id="10fc4-102">continue (C# Reference)</span></span>

<span data-ttu-id="10fc4-103">L’instruction `continue` passe le contrôle à l’itération suivante de l’instruction [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md) ou [foreach](../../../csharp/language-reference/keywords/foreach-in.md) englobante dans laquelle elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="10fc4-103">The `continue` statement passes control to the next iteration of the enclosing [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md), or [foreach](../../../csharp/language-reference/keywords/foreach-in.md) statement in which it appears.</span></span>

## <a name="example"></a><span data-ttu-id="10fc4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="10fc4-104">Example</span></span>

<span data-ttu-id="10fc4-105">Dans cet exemple, un compteur est initialisé pour compter de 1 à 10.</span><span class="sxs-lookup"><span data-stu-id="10fc4-105">In this example, a counter is initialized to count from 1 to 10.</span></span> <span data-ttu-id="10fc4-106">Si vous utilisez l’instruction `continue` conjointement avec l’expression `(i < 9)`, les instructions entre `continue` et la fin du corps de `for` sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="10fc4-106">By using the `continue` statement in conjunction with the expression `(i < 9)`, the statements between `continue` and the end of the `for` body are skipped.</span></span>

[!code-csharp[csrefKeywordsJump#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#3)]

## <a name="c-language-specification"></a><span data-ttu-id="10fc4-107">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="10fc4-107">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="10fc4-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10fc4-108">See also</span></span>

- [<span data-ttu-id="10fc4-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="10fc4-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="10fc4-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="10fc4-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="10fc4-111">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="10fc4-111">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)
- [<span data-ttu-id="10fc4-112">Instruction break</span><span class="sxs-lookup"><span data-stu-id="10fc4-112">break Statement</span></span>](/cpp/cpp/break-statement-cpp)
- [<span data-ttu-id="10fc4-113">Instructions de saut</span><span class="sxs-lookup"><span data-stu-id="10fc4-113">Jump Statements</span></span>](../../../csharp/language-reference/keywords/jump-statements.md)
