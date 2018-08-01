---
title: Gérer des exceptions dans des expressions de requête (LINQ en C#)
description: Découvrez comment gérer des exceptions dans des expressions de requête LINQ en C#.
ms.date: 12/1/2016
ms.assetid: 2bf0c397-13fb-4f68-bc2b-531c6c88a167
ms.openlocfilehash: 344d11129814516a5ed3dcf0eba73a5ecbb96981
ms.sourcegitcommit: 4c158beee818c408d45a9609bfc06f209a523e22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37403837"
---
# <a name="handle-exceptions-in-query-expressions"></a><span data-ttu-id="e1098-103">Gérer des exceptions dans des expressions de requête</span><span class="sxs-lookup"><span data-stu-id="e1098-103">Handle exceptions in query expressions</span></span>

<span data-ttu-id="e1098-104">Dans le contexte d’une expression de requête, vous pouvez appeler n’importe quelle méthode.</span><span class="sxs-lookup"><span data-stu-id="e1098-104">It's possible to call any method in the context of a query expression.</span></span> <span data-ttu-id="e1098-105">Toutefois, nous vous recommandons d’éviter d’appeler une méthode dans une expression de requête susceptible de créer un effet secondaire, tel que la modification du contenu de la source de données ou la levée d’une exception.</span><span class="sxs-lookup"><span data-stu-id="e1098-105">However, we recommend that you avoid calling any method in a query expression that can create a side effect such as modifying the contents of the data source or throwing an exception.</span></span> <span data-ttu-id="e1098-106">Cet exemple montre comment éviter la levée d’exceptions lorsque vous appelez des méthodes dans une expression de requête, en respectant les directives générales .NET relatives à la gestion des exceptions.</span><span class="sxs-lookup"><span data-stu-id="e1098-106">This example shows how to avoid raising exceptions when you call methods in a query expression without violating the general .NET guidelines on exception handling.</span></span> <span data-ttu-id="e1098-107">Selon ces directives, il est acceptable d’intercepter une exception spécifique si vous comprenez pourquoi elle est levée dans un contexte donné.</span><span class="sxs-lookup"><span data-stu-id="e1098-107">Those guidelines state that it's acceptable to catch a specific exception when you understand why it's thrown in a given context.</span></span> <span data-ttu-id="e1098-108">Pour plus d’informations, consultez les [Bonnes pratiques pour les exceptions](../../standard/exceptions/best-practices-for-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="e1098-108">For more information, see [Best Practices for Exceptions](../../standard/exceptions/best-practices-for-exceptions.md).</span></span>

<span data-ttu-id="e1098-109">Le dernier exemple montre comment gérer les cas où vous devez lever une exception pendant l’exécution d’une requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-109">The final example shows how to handle those cases when you must throw an exception during execution of a query.</span></span>

## <a name="example"></a><span data-ttu-id="e1098-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1098-110">Example</span></span>

<span data-ttu-id="e1098-111">L’exemple suivant montre comment déplacer du code de gestion des exceptions en dehors d’une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-111">The following example shows how to move exception handling code outside a query expression.</span></span> <span data-ttu-id="e1098-112">Ceci est possible uniquement lorsque la méthode ne dépend pas des variables locales de la requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-112">This is only possible when the method does not depend on any variables local to the query.</span></span>

[!code-csharp[csProgGuideLINQ#10](~/samples/snippets/csharp/concepts/linq/how-to-handle-exceptions-in-query-expressions_1.cs)]

## <a name="example"></a><span data-ttu-id="e1098-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="e1098-113">Example</span></span>

<span data-ttu-id="e1098-114">Dans certains cas, la meilleure réponse à la levée d’une exception à l’intérieur d’une requête consiste à arrêter immédiatement l’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-114">In some cases, the best response to an exception that is thrown from within a query might be to stop the query execution immediately.</span></span> <span data-ttu-id="e1098-115">L’exemple suivant montre comment gérer les exceptions pouvant être levées dans le corps d’une requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-115">The following example shows how to handle exceptions that might be thrown from inside a query body.</span></span> <span data-ttu-id="e1098-116">Supposons que `SomeMethodThatMightThrow` puisse provoquer la levée d’une exception qui nécessite l’arrêt de l’exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-116">Assume that `SomeMethodThatMightThrow` can potentially cause an exception that requires the query execution to stop.</span></span>

<span data-ttu-id="e1098-117">Notez que le bloc `try` englobe la boucle `foreach` et non la requête.</span><span class="sxs-lookup"><span data-stu-id="e1098-117">Note that the `try` block encloses the `foreach` loop, and not the query itself.</span></span> <span data-ttu-id="e1098-118">Ceci s’explique par le fait que c’est au niveau de la boucle `foreach` que la requête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="e1098-118">This is because the `foreach` loop is the point at which the query is actually executed.</span></span> <span data-ttu-id="e1098-119">Pour plus d’informations, consultez [Introduction aux requêtes LINQ](../programming-guide/concepts/linq/introduction-to-linq-queries.md).</span><span class="sxs-lookup"><span data-stu-id="e1098-119">For more information, see [Introduction to LINQ queries](../programming-guide/concepts/linq/introduction-to-linq-queries.md).</span></span>

[!code-csharp[csProgGuideLINQ#12](~/samples/snippets/csharp/concepts/linq/how-to-handle-exceptions-in-query-expressions_2.cs)]

## <a name="see-also"></a><span data-ttu-id="e1098-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1098-120">See also</span></span>

[<span data-ttu-id="e1098-121">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="e1098-121">Language Integrated Query (LINQ)</span></span>](index.md)  
