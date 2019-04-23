---
title: 'Procédure : Détecter et résoudre des soumissions en conflit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 91e27206-01fb-4c7a-8afc-1383a6ac5067
ms.openlocfilehash: 606231449263f1c26596ca8606a88053c6aded8e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138123"
---
# <a name="how-to-detect-and-resolve-conflicting-submissions"></a><span data-ttu-id="c9dd4-102">Procédure : Détecter et résoudre des soumissions en conflit</span><span class="sxs-lookup"><span data-stu-id="c9dd4-102">How to: Detect and Resolve Conflicting Submissions</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="c9dd4-103">fournit de nombreuses ressources pour détecter et résoudre des conflits issus de modifications effectuées par plusieurs utilisateurs dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="c9dd4-103">provides many resources for detecting and resolving conflicts that stem from multi-user changes to the database.</span></span> <span data-ttu-id="c9dd4-104">Pour plus d'informations, voir [Procédure : Gérer les conflits de changement](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md).</span><span class="sxs-lookup"><span data-stu-id="c9dd4-104">For more information, see [How to: Manage Change Conflicts](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9dd4-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="c9dd4-105">Example</span></span>  
 <span data-ttu-id="c9dd4-106">L’exemple suivant montre un `try` / `catch` bloc qui intercepte un <xref:System.Data.Linq.ChangeConflictException> exception.</span><span class="sxs-lookup"><span data-stu-id="c9dd4-106">The following example shows a `try`/`catch` block that catches a <xref:System.Data.Linq.ChangeConflictException> exception.</span></span> <span data-ttu-id="c9dd4-107">La fenêtre de console affiche des informations sur les entités et les membres de chaque conflit.</span><span class="sxs-lookup"><span data-stu-id="c9dd4-107">Entity and member information for each conflict is displayed in the console window.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c9dd4-108">Vous devez inclure la directive `using System.Reflection` (`Imports System.Reflection` dans Visual Basic) pour prendre en charge la récupération d'informations.</span><span class="sxs-lookup"><span data-stu-id="c9dd4-108">You must include the `using System.Reflection` directive (`Imports System.Reflection` in Visual Basic) to support the information retrieval.</span></span> <span data-ttu-id="c9dd4-109">Pour plus d'informations, consultez <xref:System.Reflection>.</span><span class="sxs-lookup"><span data-stu-id="c9dd4-109">For more information, see <xref:System.Reflection>.</span></span>  
  
 [!code-csharp[DLinqSubmittingChanges#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#2)]
 [!code-vb[DLinqSubmittingChanges#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="c9dd4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9dd4-110">See also</span></span>

- [<span data-ttu-id="c9dd4-111">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="c9dd4-111">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
- [<span data-ttu-id="c9dd4-112">Guide pratique pour Gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="c9dd4-112">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
