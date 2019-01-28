---
title: Effectuer des opérations de jointure à l'aide de clés composites (LINQ en C#)
description: Découvrez comment effectuer des opérations de jointure à l'aide de clés composites dans LINQ.
ms.date: 12/01/2016
ms.assetid: da70b54d-3213-45eb-8437-fbe75cbcf935
ms.openlocfilehash: 460a52da7e0c0a47b77d4c64e76641bae9da7cd6
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857513"
---
# <a name="join-by-using-composite-keys"></a><span data-ttu-id="55c8f-103">Effectuer des jointures à l’aide de clés composites</span><span class="sxs-lookup"><span data-stu-id="55c8f-103">Join by using composite keys</span></span>

<span data-ttu-id="55c8f-104">Cet exemple montre comment effectuer des opérations de jointure où vous voulez utiliser plusieurs clés pour définir une correspondance.</span><span class="sxs-lookup"><span data-stu-id="55c8f-104">This example shows how to perform join operations in which you want to use more than one key to define a match.</span></span> <span data-ttu-id="55c8f-105">Ceci s’effectue à l’aide d’une clé composite.</span><span class="sxs-lookup"><span data-stu-id="55c8f-105">This is accomplished by using a composite key.</span></span> <span data-ttu-id="55c8f-106">Vous créez une clé composite en tant que type anonyme ou typé nommé avec les valeurs que vous voulez comparer.</span><span class="sxs-lookup"><span data-stu-id="55c8f-106">You create a composite key as an anonymous type or named typed with the values that you want to compare.</span></span> <span data-ttu-id="55c8f-107">Si la variable de requête doit être passée au-delà des limites de la méthode, utilisez un type nommé qui substitue <xref:System.Object.Equals%2A> et <xref:System.Object.GetHashCode%2A> pour la clé.</span><span class="sxs-lookup"><span data-stu-id="55c8f-107">If the query variable will be passed across method boundaries, use a named type that overrides <xref:System.Object.Equals%2A> and <xref:System.Object.GetHashCode%2A> for the key.</span></span> <span data-ttu-id="55c8f-108">Les noms des propriétés et l’ordre dans lequel elles se trouvent doivent être identiques dans chaque clé.</span><span class="sxs-lookup"><span data-stu-id="55c8f-108">The names of the properties, and the order in which they occur, must be identical in each key.</span></span>

## <a name="example"></a><span data-ttu-id="55c8f-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="55c8f-109">Example</span></span>

<span data-ttu-id="55c8f-110">L’exemple suivant montre comment utiliser une clé composite pour joindre les données de trois tables :</span><span class="sxs-lookup"><span data-stu-id="55c8f-110">The following example demonstrates how to use a composite key to join data from three tables:</span></span>

```csharp
var query = from o in db.Orders
    from p in db.Products
    join d in db.OrderDetails
        on new {o.OrderID, p.ProductID} equals new {d.OrderID, d.ProductID} into details
        from d in details
        select new {o.OrderID, p.ProductID, d.UnitPrice};
```

<span data-ttu-id="55c8f-111">L’inférence du type sur les clés composites dépend des noms des propriétés dans les clés et l’ordre dans lequel elles apparaissent.</span><span class="sxs-lookup"><span data-stu-id="55c8f-111">Type inference on composite keys depends on the names of the properties in the keys, and the order in which they occur.</span></span> <span data-ttu-id="55c8f-112">Si les propriétés dans les séquences sources n’ont pas les mêmes noms, vous devez affecter de nouveaux noms dans les clés.</span><span class="sxs-lookup"><span data-stu-id="55c8f-112">If the properties in the source sequences don't have the same names, you must assign new names in the keys.</span></span> <span data-ttu-id="55c8f-113">Par exemple, si la table `Orders` et la table `OrderDetails` utilisent chacune des noms différents pour leurs colonnes, vous pouvez créer des clés composites en affectant des noms identiques dans les types anonymes :</span><span class="sxs-lookup"><span data-stu-id="55c8f-113">For example, if the `Orders` table and `OrderDetails` table each used different names for their columns, you could create composite keys by assigning identical names in the anonymous types:</span></span>

```csharp
join...on new {Name = o.CustomerName, ID = o.CustID} equals
    new {Name = d.CustName, ID = d.CustID }
```

<span data-ttu-id="55c8f-114">Vous pouvez aussi utiliser des clés composites dans une clause `group`.</span><span class="sxs-lookup"><span data-stu-id="55c8f-114">Composite keys can be also used in a `group` clause.</span></span>

## <a name="see-also"></a><span data-ttu-id="55c8f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55c8f-115">See also</span></span>

- [<span data-ttu-id="55c8f-116">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="55c8f-116">Language Integrated Query (LINQ)</span></span>](index.md)
- [<span data-ttu-id="55c8f-117">join, clause</span><span class="sxs-lookup"><span data-stu-id="55c8f-117">join clause</span></span>](../language-reference/keywords/join-clause.md)
- [<span data-ttu-id="55c8f-118">group, clause</span><span class="sxs-lookup"><span data-stu-id="55c8f-118">group clause</span></span>](../language-reference/keywords/group-clause.md)
