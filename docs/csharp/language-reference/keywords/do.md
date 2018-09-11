---
title: do (référence C#)
ms.date: 05/28/2018
f1_keywords:
- do_CSharpKeyword
- do
helpviewer_keywords:
- do keyword [C#]
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
ms.openlocfilehash: 89c13f5b547c13052e229ff6eb3a39ae5babce41
ms.sourcegitcommit: 4b6490b2529707627ad77c3a43fbe64120397175
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2018
ms.locfileid: "44266681"
---
# <a name="do-c-reference"></a><span data-ttu-id="22dd8-102">do (référence C#)</span><span class="sxs-lookup"><span data-stu-id="22dd8-102">do (C# Reference)</span></span>

<span data-ttu-id="22dd8-103">L’instruction `do` exécute une instruction ou un bloc d’instructions jusqu’à ce qu’une expression booléenne spécifique corresponde à la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="22dd8-103">The `do` statement executes a statement or a block of statements while a specified boolean expression evaluates to `true`.</span></span> <span data-ttu-id="22dd8-104">Dans la mesure où cette expression est évaluée après chaque exécution de la boucle, une boucle `do-while` s’exécute une ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="22dd8-104">Because that expression is evaluated after each execution of the loop, a `do-while` loop executes one or more times.</span></span> <span data-ttu-id="22dd8-105">Cela diffère de la boucle [while](while.md), qui s’exécute zéro ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="22dd8-105">This differs from the [while](while.md) loop, which executes zero or more times.</span></span>

<span data-ttu-id="22dd8-106">À tout moment dans le bloc d’instructions `do`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md).</span><span class="sxs-lookup"><span data-stu-id="22dd8-106">At any point within the `do` statement block, you can break out of the loop by using the [break](break.md) statement.</span></span>

<span data-ttu-id="22dd8-107">Vous pouvez passer directement à l’évaluation de l’expression `while` à l’aide de l’instruction [continue](continue.md).</span><span class="sxs-lookup"><span data-stu-id="22dd8-107">You can step directly to the evaluation of the `while` expression by using the [continue](continue.md) statement.</span></span> <span data-ttu-id="22dd8-108">Si l’expression correspond à `true`, l’exécution passe à la première instruction de la boucle.</span><span class="sxs-lookup"><span data-stu-id="22dd8-108">If the expression evaluates to `true`, execution continues at the first statement in the loop.</span></span> <span data-ttu-id="22dd8-109">Sinon, l’exécution passe à la première instruction après la boucle.</span><span class="sxs-lookup"><span data-stu-id="22dd8-109">Otherwise, execution continues at the first statement after the loop.</span></span>

<span data-ttu-id="22dd8-110">Vous pouvez également quitter une boucle `do-while` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).</span><span class="sxs-lookup"><span data-stu-id="22dd8-110">You also can exit a `do-while` loop by the [goto](goto.md), [return](return.md), or [throw](throw.md) statements.</span></span>

## <a name="example"></a><span data-ttu-id="22dd8-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="22dd8-111">Example</span></span>

<span data-ttu-id="22dd8-112">L’exemple suivant illustre l’utilisation de l’instruction `do`.</span><span class="sxs-lookup"><span data-stu-id="22dd8-112">The following example shows the usage of the `do` statement.</span></span> <span data-ttu-id="22dd8-113">Sélectionnez **Exécuter** pour exécuter l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="22dd8-113">Select **Run** to run the example code.</span></span> <span data-ttu-id="22dd8-114">Après cela, vous pouvez modifier le code et le réexécuter.</span><span class="sxs-lookup"><span data-stu-id="22dd8-114">After that you can modify the code and run it again.</span></span>

[!code-csharp-interactive[do loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#4)]

## <a name="c-language-specification"></a><span data-ttu-id="22dd8-115">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="22dd8-115">C# language specification</span></span>

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="22dd8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22dd8-116">See also</span></span>

- [<span data-ttu-id="22dd8-117">Référence C#</span><span class="sxs-lookup"><span data-stu-id="22dd8-117">C# Reference</span></span>](../index.md)  
- [<span data-ttu-id="22dd8-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="22dd8-118">C# Programming Guide</span></span>](../../programming-guide/index.md)  
- [<span data-ttu-id="22dd8-119">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="22dd8-119">C# Keywords</span></span>](index.md)  
- [<span data-ttu-id="22dd8-120">do-while, instruction (C++)</span><span class="sxs-lookup"><span data-stu-id="22dd8-120">do-while Statement (C++)</span></span>](/cpp/cpp/do-while-statement-cpp)  
- [<span data-ttu-id="22dd8-121">Instructions d’itération</span><span class="sxs-lookup"><span data-stu-id="22dd8-121">Iteration Statements</span></span>](iteration-statements.md)  
- [<span data-ttu-id="22dd8-122">instruction while</span><span class="sxs-lookup"><span data-stu-id="22dd8-122">while statement</span></span>](while.md)  
