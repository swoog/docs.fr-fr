---
title: 'Comment : rechercher la valeur minimale dans une séquence numérique'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 78203093-f242-4572-9b31-9495b10926aa
ms.openlocfilehash: 84002609c550cc2de76f9948bf77f9fd88261f64
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62038452"
---
# <a name="find-the-minimum-value-in-a-numeric-sequence"></a><span data-ttu-id="5dd6a-102">Comment : rechercher la valeur minimale dans une séquence numérique</span><span class="sxs-lookup"><span data-stu-id="5dd6a-102">Find the Minimum Value in a Numeric Sequence</span></span>
<span data-ttu-id="5dd6a-103">Utilisez l'opérateur <xref:System.Linq.Enumerable.Min%2A> pour retourner la valeur minimale d'une séquence de valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-103">Use the <xref:System.Linq.Enumerable.Min%2A> operator to return the minimum value from a sequence of numeric values.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5dd6a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dd6a-104">Example</span></span>  
 <span data-ttu-id="5dd6a-105">L'exemple suivant recherche le prix unitaire le plus bas parmi les produits.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-105">The following example finds the lowest unit price of any product.</span></span>  
  
 <span data-ttu-id="5dd6a-106">Si vous exécutez cette requête sur l'exemple de base de données Northwind, vous obtenez le résultat suivant : `2.5000`.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-106">If you run this query against the Northwind sample database, the output is: `2.5000`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#9](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#9)]
 [!code-vb[DLinqQueryExamples#9](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#9)]  
  
## <a name="example"></a><span data-ttu-id="5dd6a-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dd6a-107">Example</span></span>  
 <span data-ttu-id="5dd6a-108">L'exemple suivant recherche le montant de fret le plus bas parmi les commandes.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-108">The following example finds the lowest freight amount for any order.</span></span>  
  
 <span data-ttu-id="5dd6a-109">Si vous exécutez cette requête sur l'exemple de base de données Northwind, vous obtenez le résultat suivant : `0.0200`.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-109">If you run this query against the Northwind sample database, the output is: `0.0200`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#10](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#10)]
 [!code-vb[DLinqQueryExamples#10](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#10)]  
  
## <a name="example"></a><span data-ttu-id="5dd6a-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dd6a-110">Example</span></span>  
 <span data-ttu-id="5dd6a-111">L'exemple suivant utilise Min pour trouver les `Products` qui ont le prix unitaire le plus bas dans chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-111">The following example uses Min to find the `Products` that have the lowest unit price in each category.</span></span> <span data-ttu-id="5dd6a-112">La sortie est classée par catégorie.</span><span class="sxs-lookup"><span data-stu-id="5dd6a-112">The output is arranged by category.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#11](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#11)]
 [!code-vb[DLinqQueryExamples#11](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#11)]  
  
 <span data-ttu-id="5dd6a-113">Si vous exécutez la requête précédente sur l'exemple de base de données Northwind, les résultats se présenteront comme suit :</span><span class="sxs-lookup"><span data-stu-id="5dd6a-113">If you run the previous query against the Northwind sample database, your results will resemble the following:</span></span>  
  
 `1`  
  
 `Guaraná Fantástica`  
  
 `2`  
  
 `Aniseed Syrup`  
  
 `3`  
  
 `Teatime Chocolate Biscuits`  
  
 `4`  
  
 `Geitost`  
  
 `5`  
  
 `Filo Mix`  
  
 `6`  
  
 `Tourtière`  
  
 `7`  
  
 `Longlife Tofu`  
  
 `8`  
  
 `Konbu`  
  
## <a name="see-also"></a><span data-ttu-id="5dd6a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dd6a-114">See also</span></span>

- [<span data-ttu-id="5dd6a-115">Requêtes d’agrégation</span><span class="sxs-lookup"><span data-stu-id="5dd6a-115">Aggregate Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/aggregate-queries.md)
- [<span data-ttu-id="5dd6a-116">Téléchargement d’exemples de base de données</span><span class="sxs-lookup"><span data-stu-id="5dd6a-116">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
