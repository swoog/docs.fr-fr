---
title: 'Comment : récupérer des informations en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fb09e298-0b53-47e5-97fb-ab318bcd4fad
ms.openlocfilehash: dd3a510339bca8649f5654d00a9cbdfba156d92c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33360698"
---
# <a name="how-to-retrieve-information-as-read-only"></a><span data-ttu-id="3a0c8-102">Comment : récupérer des informations en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a0c8-102">How to: Retrieve Information As Read-Only</span></span>
<span data-ttu-id="3a0c8-103">Lorsque vous ne projetez pas de modifier les données, vous pouvez augmenter les performances des requêtes en recherchant des résultats en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3a0c8-103">When you do not intend to change the data, you can increase the performance of queries by seeking read-only results.</span></span>  
  
 <span data-ttu-id="3a0c8-104">Implémentez le traitement en lecture seule en affectant la valeur <xref:System.Data.Linq.DataContext.ObjectTrackingEnabled%2A> à `false`.</span><span class="sxs-lookup"><span data-stu-id="3a0c8-104">You implement read-only processing by setting <xref:System.Data.Linq.DataContext.ObjectTrackingEnabled%2A> to `false`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3a0c8-105">Lorsque la valeur <xref:System.Data.Linq.DataContext.ObjectTrackingEnabled%2A> est affectée à `false`, <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> a implicitement la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="3a0c8-105">When <xref:System.Data.Linq.DataContext.ObjectTrackingEnabled%2A> is set to `false`, <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> is implicitly set to `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3a0c8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a0c8-106">Example</span></span>  
 <span data-ttu-id="3a0c8-107">Le code suivant récupère une collection en lecture seule de dates d’embauche d’employés.</span><span class="sxs-lookup"><span data-stu-id="3a0c8-107">The following code retrieves a read-only collection of employee hire dates.</span></span>  
  
 [!code-csharp[DLinqQuerying#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#2)]
 [!code-vb[DLinqQuerying#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="3a0c8-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a0c8-108">See Also</span></span>  
 [<span data-ttu-id="3a0c8-109">Concepts relatifs aux requêtes</span><span class="sxs-lookup"><span data-stu-id="3a0c8-109">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)  
 [<span data-ttu-id="3a0c8-110">Interrogation de la base de données</span><span class="sxs-lookup"><span data-stu-id="3a0c8-110">Querying the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)  
 [<span data-ttu-id="3a0c8-111">Comparaison entre le chargement différé et le chargement immédiat</span><span class="sxs-lookup"><span data-stu-id="3a0c8-111">Deferred versus Immediate Loading</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md)
