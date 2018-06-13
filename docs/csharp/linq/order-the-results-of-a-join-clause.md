---
title: Classer les résultats d’une clause join
description: Guide pratique pour classer les résultats d’une clause join.
ms.date: 12/1/2016
ms.assetid: a7458901-1201-4c25-b8d9-c04ca52e0eb9
ms.openlocfilehash: f426152e614ed9a9c4aa41d7ba7cb8ddf1cd3063
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33269698"
---
# <a name="order-the-results-of-a-join-clause"></a><span data-ttu-id="c063d-103">Classer les résultats d’une clause join</span><span class="sxs-lookup"><span data-stu-id="c063d-103">Order the results of a join clause</span></span>
<span data-ttu-id="c063d-104">Cet exemple montre comment classer les résultats d’une opération de jointure.</span><span class="sxs-lookup"><span data-stu-id="c063d-104">This example shows how to order the results of a join operation.</span></span> <span data-ttu-id="c063d-105">Notez que le classement est effectué après la jointure.</span><span class="sxs-lookup"><span data-stu-id="c063d-105">Note that the ordering is performed after the join.</span></span> <span data-ttu-id="c063d-106">Vous pouvez utiliser une clause `orderby` avec une ou plusieurs séquences sources avant la jointure, mais cette pratique est généralement déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c063d-106">Although you can use an `orderby` clause with one or more of the source sequences before the join, generally we do not recommend it.</span></span> <span data-ttu-id="c063d-107">Certains fournisseurs LINQ ne conservent pas ce classement après la jointure.</span><span class="sxs-lookup"><span data-stu-id="c063d-107">Some LINQ providers might not preserve that ordering after the join.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c063d-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="c063d-108">Example</span></span>  
 <span data-ttu-id="c063d-109">Cette requête crée une jointure groupée, puis trie les groupes en fonction de l’élément de catégorie, qui est encore dans la portée.</span><span class="sxs-lookup"><span data-stu-id="c063d-109">This query creates a group join, and then sorts the groups based on the category element, which is still in scope.</span></span> <span data-ttu-id="c063d-110">À l’intérieur de l’initialiseur de type anonyme, une sous-requête classe tous les éléments correspondants de la séquence de produits.</span><span class="sxs-lookup"><span data-stu-id="c063d-110">Inside the anonymous type initializer, a sub-query orders all the matching elements from the products sequence.</span></span>  
  
 [!code-csharp[csProgGuideLINQ#81](../../../samples/snippets/csharp/concepts/linq/how-to-order-the-results-of-a-join-clause_1.cs)]  
 
## <a name="see-also"></a><span data-ttu-id="c063d-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c063d-111">See also</span></span>  
 [<span data-ttu-id="c063d-112">Expressions de requête LINQ</span><span class="sxs-lookup"><span data-stu-id="c063d-112">LINQ query expressions</span></span>](index.md)  
 [<span data-ttu-id="c063d-113">orderby, clause</span><span class="sxs-lookup"><span data-stu-id="c063d-113">orderby clause</span></span>](../language-reference/keywords/orderby-clause.md)  
 [<span data-ttu-id="c063d-114">join, clause</span><span class="sxs-lookup"><span data-stu-id="c063d-114">join clause</span></span>](../language-reference/keywords/join-clause.md) 
