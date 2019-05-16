---
title: 'Exceptions : try...with (expression)'
description: Découvrez comment utiliser le F# 'try... with' expression pour la gestion des exceptions.
ms.date: 05/16/2016
ms.openlocfilehash: 3ba13227ac55eff770ceb7631d3406ad80b6ea45
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641935"
---
# <a name="exceptions-the-trywith-expression"></a><span data-ttu-id="806df-103">Exceptions : try...with (expression)</span><span class="sxs-lookup"><span data-stu-id="806df-103">Exceptions: The try...with Expression</span></span>

<span data-ttu-id="806df-104">Cette rubrique décrit la `try...with` expression, l’expression qui est utilisée pour la gestion des exceptions dans le F# langage.</span><span class="sxs-lookup"><span data-stu-id="806df-104">This topic describes the `try...with` expression, the expression that is used for exception handling in the F# language.</span></span>

## <a name="syntax"></a><span data-ttu-id="806df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="806df-105">Syntax</span></span>

```fsharp
try
    expression1
with
| pattern1 -> expression2
| pattern2 -> expression3
...
```

## <a name="remarks"></a><span data-ttu-id="806df-106">Notes</span><span class="sxs-lookup"><span data-stu-id="806df-106">Remarks</span></span>

<span data-ttu-id="806df-107">Le `try...with` expression est utilisée pour gérer des exceptions dans F#.</span><span class="sxs-lookup"><span data-stu-id="806df-107">The `try...with` expression is used to handle exceptions in F#.</span></span> <span data-ttu-id="806df-108">Elle est similaire à la `try...catch` instruction en langage c#.</span><span class="sxs-lookup"><span data-stu-id="806df-108">It is similar to the `try...catch` statement in C#.</span></span> <span data-ttu-id="806df-109">Dans la syntaxe précédente, le code dans *expression1* peut générer une exception.</span><span class="sxs-lookup"><span data-stu-id="806df-109">In the preceding syntax, the code in *expression1* might generate an exception.</span></span> <span data-ttu-id="806df-110">Le `try...with` expression retourne une valeur.</span><span class="sxs-lookup"><span data-stu-id="806df-110">The `try...with` expression returns a value.</span></span> <span data-ttu-id="806df-111">Si aucune exception n’est levée, l’expression entière retourne la valeur de *expression1*.</span><span class="sxs-lookup"><span data-stu-id="806df-111">If no exception is thrown, the whole expression returns the value of *expression1*.</span></span> <span data-ttu-id="806df-112">Si une exception est levée, chacun *modèle* est ensuite comparé avec l’exception et pour le premier modèle correspondant, correspondant *expression*, connu sous le *Gestionnaire d’exceptions*, pour cette branche est exécutée, et l’expression globale retourne la valeur de l’expression dans ce gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="806df-112">If an exception is thrown, each *pattern* is compared in turn with the exception, and for the first matching pattern, the corresponding *expression*, known as the *exception handler*, for that branch is executed, and the overall expression returns the value of the expression in that exception handler.</span></span> <span data-ttu-id="806df-113">Si aucun modèle ne correspond, l’exception se propage la pile des appels jusqu'à ce qu’un gestionnaire correspondant est trouvé.</span><span class="sxs-lookup"><span data-stu-id="806df-113">If no pattern matches, the exception propagates up the call stack until a matching handler is found.</span></span> <span data-ttu-id="806df-114">Les types des valeurs retournées de chaque expression dans les gestionnaires d’exceptions doivent correspondre au type retourné à partir de l’expression dans le `try` bloc.</span><span class="sxs-lookup"><span data-stu-id="806df-114">The types of the values returned from each expression in the exception handlers must match the type returned from the expression in the `try` block.</span></span>

<span data-ttu-id="806df-115">Fréquemment, le fait qu’une erreur s’est produite également signifie qu’il n’existe aucune valeur valide qui peut être retournée par les expressions dans chaque gestionnaire d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="806df-115">Frequently, the fact that an error occurred also means that there is no valid value that can be returned from the expressions in each exception handler.</span></span> <span data-ttu-id="806df-116">Un modèle fréquent consiste à avoir le type de l’expression à être un type d’option.</span><span class="sxs-lookup"><span data-stu-id="806df-116">A frequent pattern is to have the type of the expression be an option type.</span></span> <span data-ttu-id="806df-117">L’exemple de code suivant illustre ce modèle.</span><span class="sxs-lookup"><span data-stu-id="806df-117">The following code example illustrates this pattern.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5601.fs)]

<span data-ttu-id="806df-118">Les exceptions peuvent être des exceptions .NET, ou ils peuvent être F# exceptions.</span><span class="sxs-lookup"><span data-stu-id="806df-118">Exceptions can be .NET exceptions, or they can be F# exceptions.</span></span> <span data-ttu-id="806df-119">Vous pouvez définir F# exceptions à l’aide de la `exception` mot clé.</span><span class="sxs-lookup"><span data-stu-id="806df-119">You can define F# exceptions by using the `exception` keyword.</span></span>

<span data-ttu-id="806df-120">Vous pouvez utiliser divers modèles de filtrer sur le type d’exception et d’autres conditions ; les options sont résumées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="806df-120">You can use a variety of patterns to filter on the exception type and other conditions; the options are summarized in the following table.</span></span>

|<span data-ttu-id="806df-121">Motif</span><span class="sxs-lookup"><span data-stu-id="806df-121">Pattern</span></span>|<span data-ttu-id="806df-122">Description</span><span class="sxs-lookup"><span data-stu-id="806df-122">Description</span></span>|
|-------|-----------|
|<span data-ttu-id="806df-123">:?</span><span class="sxs-lookup"><span data-stu-id="806df-123">:?</span></span> <span data-ttu-id="806df-124">*exception-type*</span><span class="sxs-lookup"><span data-stu-id="806df-124">*exception-type*</span></span>|<span data-ttu-id="806df-125">Correspond au type d’exception .NET spécifié.</span><span class="sxs-lookup"><span data-stu-id="806df-125">Matches the specified .NET exception type.</span></span>|
|<span data-ttu-id="806df-126">:?</span><span class="sxs-lookup"><span data-stu-id="806df-126">:?</span></span> <span data-ttu-id="806df-127">*type d’exception* comme *identificateur*</span><span class="sxs-lookup"><span data-stu-id="806df-127">*exception-type* as *identifier*</span></span>|<span data-ttu-id="806df-128">Correspond au type d’exception .NET spécifié, mais donne une valeur nommée à l’exception.</span><span class="sxs-lookup"><span data-stu-id="806df-128">Matches the specified .NET exception type, but gives the exception a named value.</span></span>|
|<span data-ttu-id="806df-129">*exception-name*(*arguments*)</span><span class="sxs-lookup"><span data-stu-id="806df-129">*exception-name*(*arguments*)</span></span>|<span data-ttu-id="806df-130">Correspond à un F# type d’exception et lie les arguments.</span><span class="sxs-lookup"><span data-stu-id="806df-130">Matches an F# exception type and binds the arguments.</span></span>|
|<span data-ttu-id="806df-131">*identifier*</span><span class="sxs-lookup"><span data-stu-id="806df-131">*identifier*</span></span>|<span data-ttu-id="806df-132">Correspond à n’importe quelle exception et lie le nom à l’objet exception.</span><span class="sxs-lookup"><span data-stu-id="806df-132">Matches any exception and binds the name to the exception object.</span></span> <span data-ttu-id="806df-133">Équivalent à **: ? System.Exception comme**_identificateur_</span><span class="sxs-lookup"><span data-stu-id="806df-133">Equivalent to **:? System.Exception as**_identifier_</span></span>|
|<span data-ttu-id="806df-134">*identificateur* lorsque *condition*</span><span class="sxs-lookup"><span data-stu-id="806df-134">*identifier* when *condition*</span></span>|<span data-ttu-id="806df-135">Correspond à une exception si la condition est vraie.</span><span class="sxs-lookup"><span data-stu-id="806df-135">Matches any exception if the condition is true.</span></span>|

## <a name="examples"></a><span data-ttu-id="806df-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="806df-136">Examples</span></span>

<span data-ttu-id="806df-137">Les exemples de code suivants illustrent l’utilisation des différents modèles de gestionnaire d’exception.</span><span class="sxs-lookup"><span data-stu-id="806df-137">The following code examples illustrate the use of the various exception handler patterns.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5602.fs)]

> [!NOTE]
> <span data-ttu-id="806df-138">Le `try...with` construction est une expression distincte à partir de la `try...finally` expression.</span><span class="sxs-lookup"><span data-stu-id="806df-138">The `try...with` construct is a separate expression from the `try...finally` expression.</span></span> <span data-ttu-id="806df-139">Par conséquent, si votre code requiert à la fois un `with` bloc et un `finally` bloc, vous devez imbriquer les deux expressions.</span><span class="sxs-lookup"><span data-stu-id="806df-139">Therefore, if your code requires both a `with` block and a `finally` block, you will have to nest the two expressions.</span></span>

> [!NOTE]
> <span data-ttu-id="806df-140">Vous pouvez utiliser `try...with` dans les workflows asynchrones et autres expressions de calcul, dans lequel cas une version personnalisée de la `try...with` expression est utilisée.</span><span class="sxs-lookup"><span data-stu-id="806df-140">You can use `try...with` in asynchronous workflows and other computation expressions, in which case a customized version of the `try...with` expression is used.</span></span> <span data-ttu-id="806df-141">Pour plus d’informations, consultez [flux de travail asynchrones](../asynchronous-workflows.md), et [Expressions de calcul](../computation-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="806df-141">For more information, see [Asynchronous Workflows](../asynchronous-workflows.md), and [Computation Expressions](../computation-expressions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="806df-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="806df-142">See also</span></span>

- [<span data-ttu-id="806df-143">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="806df-143">Exception Handling</span></span>](index.md)
- [<span data-ttu-id="806df-144">Types d'exceptions</span><span class="sxs-lookup"><span data-stu-id="806df-144">Exception Types</span></span>](exception-types.md)
- [<span data-ttu-id="806df-145">Exceptions : Le `try...finally` Expression</span><span class="sxs-lookup"><span data-stu-id="806df-145">Exceptions: The `try...finally` Expression</span></span>](the-try-finally-expression.md)
