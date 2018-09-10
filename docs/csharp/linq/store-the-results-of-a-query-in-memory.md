---
title: Stocker les résultats d’une requête dans la mémoire
description: Comment enregistrer les résultats.
ms.date: 11/30/2016
ms.assetid: 5b863961-1750-4cf9-9607-acea5054d15a
ms.openlocfilehash: 98a300b2c11eb037ed4ce34caea2673a4e0f8e6b
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43525228"
---
# <a name="store-the-results-of-a-query-in-memory"></a><span data-ttu-id="52bad-103">Stocker les résultats d’une requête dans la mémoire</span><span class="sxs-lookup"><span data-stu-id="52bad-103">Store the results of a query in memory</span></span>

<span data-ttu-id="52bad-104">Une requête est en fait un ensemble d’instructions permettant de récupérer et d’organiser des données.</span><span class="sxs-lookup"><span data-stu-id="52bad-104">A query is basically a set of instructions for how to retrieve and organize data.</span></span> <span data-ttu-id="52bad-105">Les requêtes sont exécutées de manière différée, à mesure que chaque élément dans le résultat est demandé.</span><span class="sxs-lookup"><span data-stu-id="52bad-105">Queries are executed lazily, as each subsequent item in the result is requested.</span></span> <span data-ttu-id="52bad-106">Lorsque vous utilisez `foreach` pour effectuer une itération sur les résultats, les éléments sont retournés lorsque vous y accédez.</span><span class="sxs-lookup"><span data-stu-id="52bad-106">When you use `foreach` to iterate the results, items are returned as accessed.</span></span> <span data-ttu-id="52bad-107">Pour évaluer une requête et stocker ses résultats sans exécuter une boucle `foreach`, appelez simplement l’une des méthodes suivantes sur la variable de requête :</span><span class="sxs-lookup"><span data-stu-id="52bad-107">To evaluate a query and store its results without executing a `foreach` loop, just call one of the following methods on the query variable:</span></span>

- <xref:System.Linq.Enumerable.ToList%2A>

- <xref:System.Linq.Enumerable.ToArray%2A>

- <xref:System.Linq.Enumerable.ToDictionary%2A>

- <xref:System.Linq.Enumerable.ToLookup%2A>

 <span data-ttu-id="52bad-108">Lorsque vous stockez les résultats de requête, nous vous recommandons d’assigner l’objet de collection retourné à une nouvelle variable, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="52bad-108">We recommend that when you store the query results, you assign the returned collection object to a new variable as shown in the following example:</span></span>

## <a name="example"></a><span data-ttu-id="52bad-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="52bad-109">Example</span></span>

[!code-csharp[csProgGuideLINQ#25](~/samples/snippets/csharp/concepts/linq/how-to-store-the-results-of-a-query-in-memory_1.cs)]

## <a name="see-also"></a><span data-ttu-id="52bad-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52bad-110">See also</span></span>

- [<span data-ttu-id="52bad-111">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="52bad-111">Language Integrated Query (LINQ)</span></span>](index.md)