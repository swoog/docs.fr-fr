---
title: 'Procédure : Spécifier les membres dont les conflits d’accès concurrentiel doivent être vérifiés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d2cda293-1e2f-4878-af0e-5aaf0d092120
ms.openlocfilehash: 9a1b4ab2dc28c569473eddbf50b96d10298d8d3c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59310432"
---
# <a name="how-to-specify-which-members-are-tested-for-concurrency-conflicts"></a><span data-ttu-id="e9a82-102">Procédure : Spécifier les membres dont les conflits d’accès concurrentiel doivent être vérifiés</span><span class="sxs-lookup"><span data-stu-id="e9a82-102">How to: Specify Which Members are Tested for Concurrency Conflicts</span></span>
<span data-ttu-id="e9a82-103">Appliquer l’une des trois enums à la [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> propriété sur un <xref:System.Data.Linq.Mapping.ColumnAttribute> attribut pour spécifier quels membres doivent être incluses dans la mise à jour vérifie pour la détection de conflits d’accès concurrentiel optimiste.</span><span class="sxs-lookup"><span data-stu-id="e9a82-103">Apply one of three enums to the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property on a <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to specify which members are to be included in update checks for the detection of optimistic concurrency conflicts.</span></span>  
  
 <span data-ttu-id="e9a82-104">La propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> (mappée au moment du design) est utilisée avec des fonctionnalités d’accès concurrentiel à l’exécution dans [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e9a82-104">The <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property (mapped at design time) is used together with run-time concurrency features in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span> <span data-ttu-id="e9a82-105">Pour plus d’informations, consultez [d’accès concurrentiel optimiste : Vue d’ensemble](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e9a82-105">For more information, see [Optimistic Concurrency: Overview](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e9a82-106">Les valeurs membres d'origine sont comparées avec l'état actuel de la base de données tant qu'aucun membre n'est désigné comme `IsVersion=true`.</span><span class="sxs-lookup"><span data-stu-id="e9a82-106">Original member values are compared with the current database state as long as no member is designated as `IsVersion=true`.</span></span> <span data-ttu-id="e9a82-107">Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span><span class="sxs-lookup"><span data-stu-id="e9a82-107">For more information, see <xref:System.Data.Linq.Mapping.ColumnAttribute.IsVersion%2A>.</span></span>  
  
 <span data-ttu-id="e9a82-108">Pour obtenir des exemples de code, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span><span class="sxs-lookup"><span data-stu-id="e9a82-108">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span></span>  
  
### <a name="to-always-use-this-member-for-detecting-conflicts"></a><span data-ttu-id="e9a82-109">Pour utiliser systématiquement ce membre pour détecter les conflits</span><span class="sxs-lookup"><span data-stu-id="e9a82-109">To always use this member for detecting conflicts</span></span>  
  
1. <span data-ttu-id="e9a82-110">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="e9a82-110">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="e9a82-111">Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à la propriété `Always`.</span><span class="sxs-lookup"><span data-stu-id="e9a82-111">Set the <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property value to `Always`.</span></span>  
  
### <a name="to-never-use-this-member-for-detecting-conflicts"></a><span data-ttu-id="e9a82-112">Pour ne jamais utiliser ce membre pour détecter des conflits</span><span class="sxs-lookup"><span data-stu-id="e9a82-112">To never use this member for detecting conflicts</span></span>  
  
1. <span data-ttu-id="e9a82-113">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="e9a82-113">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="e9a82-114">Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à la propriété `Never`.</span><span class="sxs-lookup"><span data-stu-id="e9a82-114">Set the <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property value to `Never`.</span></span>  
  
### <a name="to-use-this-member-for-detecting-conflicts-only-when-the-application-has-changed-the-value-of-the-member"></a><span data-ttu-id="e9a82-115">Pour utiliser ce membre pour détecter des conflits uniquement lorsque l'application a modifié la valeur du membre</span><span class="sxs-lookup"><span data-stu-id="e9a82-115">To use this member for detecting conflicts only when the application has changed the value of the member</span></span>  
  
1. <span data-ttu-id="e9a82-116">Ajoutez la propriété <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à l'attribut <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="e9a82-116">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2. <span data-ttu-id="e9a82-117">Affectez la valeur <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> à la propriété `WhenChanged`.</span><span class="sxs-lookup"><span data-stu-id="e9a82-117">Set the <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A> property value to `WhenChanged`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e9a82-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="e9a82-118">Example</span></span>  
 <span data-ttu-id="e9a82-119">L'exemple suivant spécifie que les objets `HomePage` ne doivent jamais être testés pendant des contrôles de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e9a82-119">The following example specifies that `HomePage` objects should never be tested during update checks.</span></span> <span data-ttu-id="e9a82-120">Pour plus d'informations, consultez <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span><span class="sxs-lookup"><span data-stu-id="e9a82-120">For more information, see <xref:System.Data.Linq.Mapping.ColumnAttribute.UpdateCheck%2A>.</span></span>  
  
 [!code-csharp[System.Data.Linq.Mapping.UpdateCheck#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.mapping.updatecheck/cs/northwind.cs#1)]
 [!code-vb[System.Data.Linq.Mapping.UpdateCheck#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.mapping.updatecheck/vb/northwind.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="e9a82-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9a82-121">See also</span></span>

- [<span data-ttu-id="e9a82-122">Guide pratique pour Gérer les conflits de changement</span><span class="sxs-lookup"><span data-stu-id="e9a82-122">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
- [<span data-ttu-id="e9a82-123">Apport et soumission de modifications de données</span><span class="sxs-lookup"><span data-stu-id="e9a82-123">Making and Submitting Data Changes</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/making-and-submitting-data-changes.md)
