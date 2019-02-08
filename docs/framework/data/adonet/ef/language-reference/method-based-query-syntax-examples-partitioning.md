---
title: 'Exemples de syntaxe de requête fondée sur une méthode : Partitionnement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: b7b64874-c3c8-4bdb-862c-89a168d07827
ms.openlocfilehash: 181564de997e9a799aafa660a16b32a6ceb91d4a
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827148"
---
# <a name="method-based-query-syntax-examples-partitioning"></a><span data-ttu-id="787f4-102">Exemples de syntaxe de requête fondée sur une méthode : Partitionnement</span><span class="sxs-lookup"><span data-stu-id="787f4-102">Method-Based Query Syntax Examples: Partitioning</span></span>
<span data-ttu-id="787f4-103">Les exemples de cette rubrique montrent comment utiliser le <xref:System.Linq.Enumerable.Skip%2A>, et <xref:System.Linq.Enumerable.Take%2A> méthodes permettant d’interroger la [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) à l’aide de la syntaxe d’expression de requête.</span><span class="sxs-lookup"><span data-stu-id="787f4-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Skip%2A>, and <xref:System.Linq.Enumerable.Take%2A> methods to query the [AdventureWorks Sales Model](https://archive.codeplex.com/?p=msftdbprodsamples) using query expression syntax.</span></span> <span data-ttu-id="787f4-104">Le modèle de vente AdventureWorks Sales Model utilisé dans ces exemples est construit à partir des tables Contact, Address, Product, SalesOrderHeader et SalesOrderDetail de l'exemple de base de données AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="787f4-104">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="787f4-105">Les exemples de cette rubrique utilisent les éléments suivants `using` / `Imports` instructions :</span><span class="sxs-lookup"><span data-stu-id="787f4-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="skip"></a><span data-ttu-id="787f4-106">Ignorer</span><span class="sxs-lookup"><span data-stu-id="787f4-106">Skip</span></span>  
  
### <a name="example"></a><span data-ttu-id="787f4-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="787f4-107">Example</span></span>  
 <span data-ttu-id="787f4-108">L'exemple suivant utilise la méthode <xref:System.Linq.Enumerable.Skip%2A> pour obtenir tous les contacts de la table Contact, à l'exception des cinq premiers.</span><span class="sxs-lookup"><span data-stu-id="787f4-108">The following example uses the <xref:System.Linq.Enumerable.Skip%2A> method to get all but the first five contacts of the Contact table.</span></span>  
  
 [!code-csharp[DP L2E Examples#SkipSimple](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#skipsimple)]
 [!code-vb[DP L2E Examples#SkipSimple](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#skipsimple)]  
  
### <a name="example"></a><span data-ttu-id="787f4-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="787f4-109">Example</span></span>  
 <span data-ttu-id="787f4-110">L'exemple suivant utilise la méthode <xref:System.Linq.Enumerable.Skip%2A> pour obtenir toutes les adresses de Seattle, à l'exception des deux premières.</span><span class="sxs-lookup"><span data-stu-id="787f4-110">The following example uses the <xref:System.Linq.Enumerable.Skip%2A> method to get all but the first two addresses in Seattle.</span></span>  
  
 [!code-csharp[DP L2E Examples#SkipNested](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#skipnested)]
 [!code-vb[DP L2E Examples#SkipNested](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#skipnested)]  
  
## <a name="take"></a><span data-ttu-id="787f4-111">Take</span><span class="sxs-lookup"><span data-stu-id="787f4-111">Take</span></span>  
  
### <a name="example"></a><span data-ttu-id="787f4-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="787f4-112">Example</span></span>  
 <span data-ttu-id="787f4-113">L'exemple suivant utilise la méthode <xref:System.Linq.Enumerable.Take%2A> pour obtenir uniquement les cinq premiers contacts de la table Contact.</span><span class="sxs-lookup"><span data-stu-id="787f4-113">The following example uses the <xref:System.Linq.Enumerable.Take%2A> method to get only the first five contacts from the Contact table.</span></span>  
  
 [!code-csharp[DP L2E Examples#TakeSimple](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#takesimple)]
 [!code-vb[DP L2E Examples#TakeSimple](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#takesimple)]  
  
### <a name="example"></a><span data-ttu-id="787f4-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="787f4-114">Example</span></span>  
 <span data-ttu-id="787f4-115">L'exemple suivant utilise la méthode <xref:System.Linq.Enumerable.Take%2A> pour obtenir les trois premières adresses de Seattle.</span><span class="sxs-lookup"><span data-stu-id="787f4-115">The following example uses the <xref:System.Linq.Enumerable.Take%2A> method to get the first three addresses in Seattle.</span></span>  
  
 [!code-csharp[DP L2E Examples#TakeNested](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#takenested)]
 [!code-vb[DP L2E Examples#TakeNested](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#takenested)]  
  
## <a name="see-also"></a><span data-ttu-id="787f4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="787f4-116">See also</span></span>
- [<span data-ttu-id="787f4-117">Requêtes dans LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="787f4-117">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
