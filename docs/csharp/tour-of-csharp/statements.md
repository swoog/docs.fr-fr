---
title: Instructions C# - Visite guidée du langage C#
description: Vous créez les actions d’un programme C# à l’aide d’instructions
ms.date: 11/06/2016
ms.assetid: 5409c379-5622-4fae-88b5-1654276ea8d4
ms.openlocfilehash: 2f25c07ccc0af27a503465b9414bf607c61d1b2e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33351977"
---
# <a name="statements"></a><span data-ttu-id="bbb56-103">Instructions</span><span class="sxs-lookup"><span data-stu-id="bbb56-103">Statements</span></span>

<span data-ttu-id="bbb56-104">Les actions d’un programme sont exprimées à l’aide *d’instructions*.</span><span class="sxs-lookup"><span data-stu-id="bbb56-104">The actions of a program are expressed using *statements*.</span></span> <span data-ttu-id="bbb56-105">C# prend en charge plusieurs types d’instructions, dont plusieurs sont définies en termes d’instructions incorporées.</span><span class="sxs-lookup"><span data-stu-id="bbb56-105">C# supports several different kinds of statements, a number of which are defined in terms of embedded statements.</span></span>

<span data-ttu-id="bbb56-106">Un *bloc* autorise l’écriture de plusieurs instructions dans les contextes où une seule instruction est autorisée.</span><span class="sxs-lookup"><span data-stu-id="bbb56-106">A *block* permits multiple statements to be written in contexts where a single statement is allowed.</span></span> <span data-ttu-id="bbb56-107">Un bloc se compose d’une liste d’instructions écrites entre les délimiteurs `{` et `}`.</span><span class="sxs-lookup"><span data-stu-id="bbb56-107">A block consists of a list of statements written between the delimiters `{` and `}`.</span></span>

<span data-ttu-id="bbb56-108">Les *instructions de déclaration* sont utilisées pour déclarer des variables locales et des constantes.</span><span class="sxs-lookup"><span data-stu-id="bbb56-108">*Declaration statements* are used to declare local variables and constants.</span></span>

<span data-ttu-id="bbb56-109">Les *instructions d’expression* sont utilisées pour évaluer des expressions.</span><span class="sxs-lookup"><span data-stu-id="bbb56-109">*Expression statements* are used to evaluate expressions.</span></span> <span data-ttu-id="bbb56-110">Les expressions qui peuvent être utilisées en tant qu’instructions comprennent les appels de méthode, les allocations d’objet avec l’opérateur `new`, les affectations avec `=` et les opérateurs d’assignation composée, les opérations d’incrémentation et de décrémentation à l’aide des opérateurs `++` et `--` et les expressions `await`.</span><span class="sxs-lookup"><span data-stu-id="bbb56-110">Expressions that can be used as statements include method invocations, object allocations using the `new` operator, assignments using `=` and the compound assignment operators, increment and decrement operations using the `++` and `--` operators and `await` expressions.</span></span>

<span data-ttu-id="bbb56-111">Les *instructions de sélection* sont utilisées pour sélectionner un nombre d’instructions possibles pour l’exécution en fonction de la valeur d’une expression.</span><span class="sxs-lookup"><span data-stu-id="bbb56-111">*Selection statements* are used to select one of a number of possible statements for execution based on the value of some expression.</span></span> <span data-ttu-id="bbb56-112">Dans ce groupe, ce sont les instructions `if` et `switch`.</span><span class="sxs-lookup"><span data-stu-id="bbb56-112">In this group are the `if` and `switch` statements.</span></span>

<span data-ttu-id="bbb56-113">Les *instructions d’itération* servent à exécuter à plusieurs reprises une instruction incorporée.</span><span class="sxs-lookup"><span data-stu-id="bbb56-113">*Iteration statements* are used to execute repeatedly an embedded statement.</span></span> <span data-ttu-id="bbb56-114">Dans ce groupe, ce sont les instructions `while`, `do`, `for` et `foreach`.</span><span class="sxs-lookup"><span data-stu-id="bbb56-114">In this group are the `while`, `do`, `for`, and `foreach` statements.</span></span>

<span data-ttu-id="bbb56-115">Les *instructions de saut* sont utilisées pour transférer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="bbb56-115">*Jump statements* are used to transfer control.</span></span> <span data-ttu-id="bbb56-116">Dans ce groupe, ce sont les instructions `break`, `continue`, `goto`, `throw`, `return` et `yield`.</span><span class="sxs-lookup"><span data-stu-id="bbb56-116">In this group are the `break`, `continue`, `goto`, `throw`, `return`, and `yield` statements.</span></span>

<span data-ttu-id="bbb56-117">L’instruction `try`...`catch` est utilisée pour intercepter les exceptions qui se produisent pendant l’exécution d’un bloc, et l’instruction `try`...`finally` permet de spécifier que le code de finalisation est toujours exécuté, qu’une exception se soit produite ou non.</span><span class="sxs-lookup"><span data-stu-id="bbb56-117">The `try`...`catch` statement is used to catch exceptions that occur during execution of a block, and the `try`...`finally` statement is used to specify finalization code that is always executed, whether an exception occurred or not.</span></span>

<span data-ttu-id="bbb56-118">Les instructions `checked` et `unchecked` permettent de contrôler le contexte de dépassement de capacité pour les conversions et les opérations arithmétiques de type intégral.</span><span class="sxs-lookup"><span data-stu-id="bbb56-118">The `checked` and `unchecked` statements are used to control the overflow-checking context for integral-type arithmetic operations and conversions.</span></span>

<span data-ttu-id="bbb56-119">L’instruction `lock` est utilisée pour obtenir le verrou d’exclusion mutuelle pour un objet donné, exécuter une instruction, puis libérer le verrou.</span><span class="sxs-lookup"><span data-stu-id="bbb56-119">The `lock` statement is used to obtain the mutual-exclusion lock for a given object, execute a statement, and then release the lock.</span></span>

<span data-ttu-id="bbb56-120">L’instruction `using` est utilisée pour obtenir une ressource, exécuter une instruction puis supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="bbb56-120">The `using` statement is used to obtain a resource, execute a statement, and then dispose of that resource.</span></span>

<span data-ttu-id="bbb56-121">La liste suivante décrit les types d’instructions qui peuvent être utilisés avec un exemple pour chacun.</span><span class="sxs-lookup"><span data-stu-id="bbb56-121">The following lists the kinds of statements that can be used, and provides an example for each.</span></span>

* <span data-ttu-id="bbb56-122">Déclaration de variable locale :</span><span class="sxs-lookup"><span data-stu-id="bbb56-122">Local variable declaration:</span></span>

 [!code-csharp[Declarations](../../../samples/snippets/csharp/tour/statements/Program.cs#L9-L15)]

* <span data-ttu-id="bbb56-123">Déclaration de constante locale :</span><span class="sxs-lookup"><span data-stu-id="bbb56-123">Local constant declaration:</span></span>

 [!code-csharp[ConstantDeclarations](../../../samples/snippets/csharp/tour/statements/Program.cs#L17-L22)]

* <span data-ttu-id="bbb56-124">Instruction d’expression :</span><span class="sxs-lookup"><span data-stu-id="bbb56-124">Expression statement:</span></span>

 [!code-csharp[Expressions](../../../samples/snippets/csharp/tour/statements/Program.cs#L24-L31)]

* <span data-ttu-id="bbb56-125">Instruction `if` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-125">`if` statement:</span></span>

 [!code-csharp[IfStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L33-L43)]

* <span data-ttu-id="bbb56-126">Instruction `switch` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-126">`switch` statement:</span></span>

 [!code-csharp[SwitchStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L45-L60)]

* <span data-ttu-id="bbb56-127">Instruction `while` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-127">`while` statement:</span></span>

 [!code-csharp[WhileStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L62-L70)]

* <span data-ttu-id="bbb56-128">Instruction `do` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-128">`do` statement:</span></span>

 [!code-csharp[DoStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L72-L81)]

* <span data-ttu-id="bbb56-129">Instruction `for` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-129">`for` statement:</span></span>

 [!code-csharp[ForStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L83-L89)]

* <span data-ttu-id="bbb56-130">Instruction `foreach` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-130">`foreach` statement:</span></span>

 [!code-csharp[ForEachStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L91-L97)]

* <span data-ttu-id="bbb56-131">Instruction `break` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-131">`break` statement:</span></span>

 [!code-csharp[BreakStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L99-L108)]

* <span data-ttu-id="bbb56-132">Instruction `continue` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-132">`continue` statement:</span></span>

 [!code-csharp[ContinueStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L110-L118)]

* <span data-ttu-id="bbb56-133">Instruction `goto` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-133">`goto` statement:</span></span>

 [!code-csharp[GotoStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L120-L129)]

* <span data-ttu-id="bbb56-134">Instruction `return` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-134">`return` statement:</span></span>

 [!code-csharp[ReturnStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L131-L139)]

* <span data-ttu-id="bbb56-135">Instruction `yield` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-135">`yield` statement:</span></span>

 [!code-csharp[YieldStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L141-L155)]

* <span data-ttu-id="bbb56-136">Instructions `throw` et instructions `try` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-136">`throw` statements and `try` statements:</span></span>

 [!code-csharp[TryThrow](../../../samples/snippets/csharp/tour/statements/Program.cs#L157-L183)]

* <span data-ttu-id="bbb56-137">Instructions `checked` et `unchecked` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-137">`checked` and `unchecked` statements:</span></span>

 [!code-csharp[CheckedUncheckedStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L185-L196)]

* <span data-ttu-id="bbb56-138">Instruction `lock` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-138">`lock` statement:</span></span>

 [!code-csharp[LockStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L257-L273)]

* <span data-ttu-id="bbb56-139">Instruction `using` :</span><span class="sxs-lookup"><span data-stu-id="bbb56-139">`using` statement:</span></span>

 [!code-csharp[UsingStatement](../../../samples/snippets/csharp/tour/statements/Program.cs#L198-L206)]

>[!div class="step-by-step"]
<span data-ttu-id="bbb56-140">[Précédent](expressions.md)
[Suivant](classes-and-objects.md)</span><span class="sxs-lookup"><span data-stu-id="bbb56-140">[Previous](expressions.md)
[Next](classes-and-objects.md)</span></span>
