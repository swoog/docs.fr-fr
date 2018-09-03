---
title: while (référence C#)
ms.date: 05/28/2018
f1_keywords:
- while_CSharpKeyword
- while
helpviewer_keywords:
- while keyword [C#]
ms.assetid: 72a0765c-6852-4aca-b327-4a11cb7f5c59
ms.openlocfilehash: e3e9493b5371fbd6f53a779ba73743efc6d6e05b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43390022"
---
# <a name="while-c-reference"></a><span data-ttu-id="09bb4-102">while (référence C#)</span><span class="sxs-lookup"><span data-stu-id="09bb4-102">while (C# Reference)</span></span>

<span data-ttu-id="09bb4-103">L’instruction `while` exécute une instruction ou un bloc d’instructions jusqu’à ce qu’une expression booléenne spécifique corresponde à la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="09bb4-103">The `while` statement executes a statement or a block of statements while a specified boolean expression evaluates to `true`.</span></span> <span data-ttu-id="09bb4-104">Dans la mesure où cette expression est évaluée avant chaque exécution de la boucle, une boucle `while` s’exécute plusieurs fois ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="09bb4-104">Because that expression is evaluated before each execution of the loop, a `while` loop executes zero or more times.</span></span> <span data-ttu-id="09bb4-105">Cela diffère de la boucle [do](do.md), qui s’exécute une ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="09bb4-105">This differs from the [do](do.md) loop, which executes one or more times.</span></span>

<span data-ttu-id="09bb4-106">À tout moment dans le bloc d’instructions `while`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md).</span><span class="sxs-lookup"><span data-stu-id="09bb4-106">At any point within the `while` statement block, you can break out of the loop by using the [break](break.md) statement.</span></span>

<span data-ttu-id="09bb4-107">Vous pouvez passer directement à l’évaluation de l’expression `while` à l’aide de l’instruction [continue](continue.md).</span><span class="sxs-lookup"><span data-stu-id="09bb4-107">You can step directly to the evaluation of the `while` expression by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="09bb4-108">Si l’expression correspond à `true`, l’exécution passe à la première instruction de la boucle.</span><span class="sxs-lookup"><span data-stu-id="09bb4-108">If the expression evaluates to `true`, execution continues at the first statement in the loop.</span></span> <span data-ttu-id="09bb4-109">Sinon, l’exécution passe à la première instruction après la boucle.</span><span class="sxs-lookup"><span data-stu-id="09bb4-109">Otherwise, execution continues at the first statement after the loop.</span></span>

<span data-ttu-id="09bb4-110">Vous pouvez également quitter une boucle `while` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).</span><span class="sxs-lookup"><span data-stu-id="09bb4-110">You also can exit a `while` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="example"></a><span data-ttu-id="09bb4-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="09bb4-111">Example</span></span>

<span data-ttu-id="09bb4-112">L’exemple suivant illustre l’utilisation de l’instruction `while`.</span><span class="sxs-lookup"><span data-stu-id="09bb4-112">The following example shows the usage of the `while` statement.</span></span> <span data-ttu-id="09bb4-113">Sélectionnez **Exécuter** pour exécuter l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="09bb4-113">Select **Run** to run the example code.</span></span> <span data-ttu-id="09bb4-114">Après cela, vous pouvez modifier le code et le réexécuter.</span><span class="sxs-lookup"><span data-stu-id="09bb4-114">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[while loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#3)]

## <a name="c-language-specification"></a><span data-ttu-id="09bb4-115">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="09bb4-115">C# language specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="09bb4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09bb4-116">See also</span></span>

- [<span data-ttu-id="09bb4-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="09bb4-117">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="09bb4-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="09bb4-118">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="09bb4-119">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="09bb4-119">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="09bb4-120">while, instruction (C++)</span><span class="sxs-lookup"><span data-stu-id="09bb4-120">while Statement (C++)</span></span>](/cpp/cpp/while-statement-cpp)  
- [<span data-ttu-id="09bb4-121">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="09bb4-121">Iteration Statements</span></span>](iteration-statements.md)  
- [<span data-ttu-id="09bb4-122">Instruction do</span><span class="sxs-lookup"><span data-stu-id="09bb4-122">do statement</span></span>](do.md)  
