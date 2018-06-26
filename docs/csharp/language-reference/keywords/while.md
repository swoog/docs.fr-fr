---
title: while (référence C#)
ms.date: 05/28/2018
f1_keywords:
- while_CSharpKeyword
- while
helpviewer_keywords:
- while keyword [C#]
ms.assetid: 72a0765c-6852-4aca-b327-4a11cb7f5c59
ms.openlocfilehash: c082107472ac53d05b3b43dd4d9d8afc508a16cb
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34565863"
---
# <a name="while-c-reference"></a><span data-ttu-id="0426e-102">while (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0426e-102">while (C# Reference)</span></span>

<span data-ttu-id="0426e-103">L’instruction `while` exécute une instruction ou un bloc d’instructions jusqu’à ce qu’une expression booléenne spécifique corresponde à la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="0426e-103">The `while` statement executes a statement or a block of statements while a specified boolean expression evaluates to `true`.</span></span> <span data-ttu-id="0426e-104">Dans la mesure où cette expression est évaluée avant chaque exécution de la boucle, une boucle `while` s’exécute plusieurs fois ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="0426e-104">Because that expression is evaluated before each execution of the loop, a `while` loop executes zero or more times.</span></span> <span data-ttu-id="0426e-105">Cela diffère de la boucle [do](do.md), qui s’exécute une ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="0426e-105">This differs from the [do](do.md) loop, which executes one or more times.</span></span>

<span data-ttu-id="0426e-106">À tout moment dans le bloc d’instructions `while`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md).</span><span class="sxs-lookup"><span data-stu-id="0426e-106">At any point within the `while` statement block, you can break out of the loop by using the [break](break.md) statement.</span></span>

<span data-ttu-id="0426e-107">Vous pouvez passer directement à l’évaluation de l’expression `while` à l’aide de l’instruction [continue](continue.md).</span><span class="sxs-lookup"><span data-stu-id="0426e-107">You can step directly to the evaluation of the `while` expression by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="0426e-108">Si l’expression correspond à `true`, l’exécution passe à la première instruction de la boucle.</span><span class="sxs-lookup"><span data-stu-id="0426e-108">If the expression evaluates to `true`, execution continues at the first statement in the loop.</span></span> <span data-ttu-id="0426e-109">Sinon, l’exécution passe à la première instruction après la boucle.</span><span class="sxs-lookup"><span data-stu-id="0426e-109">Otherwise, execution continues at the first statement after the loop.</span></span>

<span data-ttu-id="0426e-110">Vous pouvez également quitter une boucle `while` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).</span><span class="sxs-lookup"><span data-stu-id="0426e-110">You also can exit a `while` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="example"></a><span data-ttu-id="0426e-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="0426e-111">Example</span></span>

<span data-ttu-id="0426e-112">L’exemple suivant illustre l’utilisation de l’instruction `while`.</span><span class="sxs-lookup"><span data-stu-id="0426e-112">The following example shows the usage of the `while` statement.</span></span> <span data-ttu-id="0426e-113">Sélectionnez **Exécuter** pour exécuter l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="0426e-113">Select **Run** to run the example code.</span></span> <span data-ttu-id="0426e-114">Après cela, vous pourrez modifier le code et le réexécuter.</span><span class="sxs-lookup"><span data-stu-id="0426e-114">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[while loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#3)]

## <a name="c-language-specification"></a><span data-ttu-id="0426e-115">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="0426e-115">C# language specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="0426e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0426e-116">See also</span></span>

 [<span data-ttu-id="0426e-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0426e-117">C# Reference</span></span>](../index.md)  
 [<span data-ttu-id="0426e-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0426e-118">C# Programming Guide</span></span>](../../programming-guide/index.md)  
 [<span data-ttu-id="0426e-119">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="0426e-119">C# Keywords</span></span>](index.md)  
 [<span data-ttu-id="0426e-120">while, instruction (C++)</span><span class="sxs-lookup"><span data-stu-id="0426e-120">while Statement (C++)</span></span>](/cpp/cpp/while-statement-cpp)  
 [<span data-ttu-id="0426e-121">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="0426e-121">Iteration Statements</span></span>](iteration-statements.md)  
 [<span data-ttu-id="0426e-122">Instruction do</span><span class="sxs-lookup"><span data-stu-id="0426e-122">do statement</span></span>](do.md)  
