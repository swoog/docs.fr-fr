---
title: do (référence C#)
ms.date: 05/28/2018
f1_keywords:
- do_CSharpKeyword
- do
helpviewer_keywords:
- do keyword [C#]
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
ms.openlocfilehash: 4dd5f4034bcd60b714071eb7eb9518e66ac0c848
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53129023"
---
# <a name="do-c-reference"></a><span data-ttu-id="9545c-102">do (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9545c-102">do (C# Reference)</span></span>

<span data-ttu-id="9545c-103">L’instruction `do` exécute une instruction ou un bloc d’instructions tant qu’une expression booléenne donne la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="9545c-103">The `do` statement executes a statement or a block of statements while a specified Boolean expression evaluates to `true`.</span></span> <span data-ttu-id="9545c-104">Dans la mesure où cette expression est évaluée après chaque exécution de la boucle, une boucle `do-while` s’exécute une ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="9545c-104">Because that expression is evaluated after each execution of the loop, a `do-while` loop executes one or more times.</span></span> <span data-ttu-id="9545c-105">Cela diffère de la boucle [while](while.md), qui s’exécute zéro ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="9545c-105">This differs from the [while](while.md) loop, which executes zero or more times.</span></span>

<span data-ttu-id="9545c-106">À tout moment dans le bloc d’instructions `do`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md).</span><span class="sxs-lookup"><span data-stu-id="9545c-106">At any point within the `do` statement block, you can break out of the loop by using the [break](break.md) statement.</span></span>

<span data-ttu-id="9545c-107">Vous pouvez passer directement à l’évaluation de l’expression `while` à l’aide de l’instruction [continue](continue.md).</span><span class="sxs-lookup"><span data-stu-id="9545c-107">You can step directly to the evaluation of the `while` expression by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="9545c-108">Si l’expression correspond à `true`, l’exécution passe à la première instruction de la boucle.</span><span class="sxs-lookup"><span data-stu-id="9545c-108">If the expression evaluates to `true`, execution continues at the first statement in the loop.</span></span> <span data-ttu-id="9545c-109">Sinon, l’exécution passe à la première instruction après la boucle.</span><span class="sxs-lookup"><span data-stu-id="9545c-109">Otherwise, execution continues at the first statement after the loop.</span></span>

<span data-ttu-id="9545c-110">Vous pouvez également quitter une boucle `do-while` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).</span><span class="sxs-lookup"><span data-stu-id="9545c-110">You also can exit a `do-while` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="example"></a><span data-ttu-id="9545c-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="9545c-111">Example</span></span>

<span data-ttu-id="9545c-112">L’exemple suivant illustre l’utilisation de l’instruction `do`.</span><span class="sxs-lookup"><span data-stu-id="9545c-112">The following example shows the usage of the `do` statement.</span></span> <span data-ttu-id="9545c-113">Sélectionnez **Exécuter** pour exécuter l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="9545c-113">Select **Run** to run the example code.</span></span> <span data-ttu-id="9545c-114">Après cela, vous pouvez modifier le code et le réexécuter.</span><span class="sxs-lookup"><span data-stu-id="9545c-114">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[do loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="9545c-115">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9545c-115">C# language specification</span></span>

<span data-ttu-id="9545c-116">Pour plus d’informations, voir la section [Instruction do](~/_csharplang/spec/statements.md#the-do-statement) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="9545c-116">For more information, see [The do statement](~/_csharplang/spec/statements.md#the-do-statement) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9545c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9545c-117">See also</span></span>

- [<span data-ttu-id="9545c-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9545c-118">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="9545c-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9545c-119">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="9545c-120">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="9545c-120">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="9545c-121">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="9545c-121">Iteration Statements</span></span>](iteration-statements.md)
- [<span data-ttu-id="9545c-122">instruction while</span><span class="sxs-lookup"><span data-stu-id="9545c-122">while statement</span></span>](while.md)
