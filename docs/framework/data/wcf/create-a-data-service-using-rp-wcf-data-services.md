---
title: 'Procédure : Créer un Service de données en utilisant le fournisseur de réflexion (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, providers
ms.assetid: 7315c6d8-f452-4fb2-a0c1-76ab0593c146
ms.openlocfilehash: 233b17de17b7f50547b2f4fbf6a543d7258183cf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765906"
---
# <a name="how-to-create-a-data-service-using-the-reflection-provider-wcf-data-services"></a><span data-ttu-id="1300d-102">Procédure : Créer un Service de données en utilisant le fournisseur de réflexion (WCF Data Services)</span><span class="sxs-lookup"><span data-stu-id="1300d-102">How to: Create a Data Service Using the Reflection Provider (WCF Data Services)</span></span>
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] <span data-ttu-id="1300d-103">vous permet de définir un modèle de données basé sur les classes arbitraires tant que ces classes sont exposées comme des objets qui implémentent l'interface <xref:System.Linq.IQueryable%601>.</span><span class="sxs-lookup"><span data-stu-id="1300d-103">enables you to define a data model that is based on arbitrary classes as long as those classes are exposed as objects that implement the <xref:System.Linq.IQueryable%601> interface.</span></span> <span data-ttu-id="1300d-104">Pour plus d’informations, consultez [fournisseurs de Services de données](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="1300d-104">For more information, see [Data Services Providers](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="1300d-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="1300d-105">Example</span></span>  
 <span data-ttu-id="1300d-106">L'exemple suivant définit un modèle de données qui inclut `Orders` et `Items`.</span><span class="sxs-lookup"><span data-stu-id="1300d-106">The following example defines a data model that includes `Orders` and `Items`.</span></span> <span data-ttu-id="1300d-107">La classe de conteneur d'entités  `OrderItemData` a deux méthodes publiques qui retournent des interfaces <xref:System.Linq.IQueryable%601>.</span><span class="sxs-lookup"><span data-stu-id="1300d-107">The entity container class `OrderItemData` has two public methods that return <xref:System.Linq.IQueryable%601> interfaces.</span></span> <span data-ttu-id="1300d-108">Ces interfaces sont les jeux d'entités des types d'entité `Orders` et `Items`.</span><span class="sxs-lookup"><span data-stu-id="1300d-108">These interfaces are the entity sets of the `Orders` and `Items` entity types.</span></span> <span data-ttu-id="1300d-109">Un `Order` peut inclure plusieurs `Items`, donc le type d’entité `Orders` a une propriété de navigation `Items` qui retourne une collection d’objets `Items`.</span><span class="sxs-lookup"><span data-stu-id="1300d-109">An `Order` can include multiple `Items`, so the `Orders` entity type has an `Items` navigation property that returns a collection of `Items` objects.</span></span> <span data-ttu-id="1300d-110">La classe de conteneur d'entités `OrderItemData` est le type générique de la classe <xref:System.Data.Services.DataService%601> d'où est dérivé le service de données `OrderItems`.</span><span class="sxs-lookup"><span data-stu-id="1300d-110">The `OrderItemData` entity container class is the generic type of the <xref:System.Data.Services.DataService%601> class from which the `OrderItems` data service is derived.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1300d-111">Comme cet exemple illustre un fournisseur de données en mémoire et que les modifications ne sont pas persistantes en dehors des instances de l'objet actuelles, l'implémentation de l'interface <xref:System.Data.Services.IUpdatable> n'apporte aucun avantage.</span><span class="sxs-lookup"><span data-stu-id="1300d-111">Because this example demonstrates an in-memory data provider and changes are not persisted outside of the current object instances, there is no benefit derived from implementing the <xref:System.Data.Services.IUpdatable> interface.</span></span> <span data-ttu-id="1300d-112">Pour obtenir un exemple qui implémente le <xref:System.Data.Services.IUpdatable> l’interface, consultez [Comment : Créer un Service de données à l’aide d’un LINQ vers la Source de données SQL](../../../../docs/framework/data/wcf/create-a-data-service-using-linq-to-sql-wcf.md).</span><span class="sxs-lookup"><span data-stu-id="1300d-112">For an example that implements the <xref:System.Data.Services.IUpdatable> interface, see [How to: Create a Data Service Using a LINQ to SQL Data Source](../../../../docs/framework/data/wcf/create-a-data-service-using-linq-to-sql-wcf.md).</span></span>  
  
 [!code-csharp[Astoria Reflection Provider#CustomIQueryable](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_reflection_provider/cs/orderitems.svc.cs#customiqueryable)]
 [!code-vb[Astoria Reflection Provider#CustomIQueryable](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_reflection_provider/vb/orderitems.svc.vb#customiqueryable)]  
  
## <a name="see-also"></a><span data-ttu-id="1300d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1300d-113">See also</span></span>

- [<span data-ttu-id="1300d-114">Guide pratique pour Créer un Service de données à l’aide d’un LINQ vers la Source de données SQL</span><span class="sxs-lookup"><span data-stu-id="1300d-114">How to: Create a Data Service Using a LINQ to SQL Data Source</span></span>](../../../../docs/framework/data/wcf/create-a-data-service-using-linq-to-sql-wcf.md)
- [<span data-ttu-id="1300d-115">Fournisseurs de services de données</span><span class="sxs-lookup"><span data-stu-id="1300d-115">Data Services Providers</span></span>](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md)
- [<span data-ttu-id="1300d-116">Guide pratique pour Créer un Service de données à l’aide d’une Source de données ADO.NET Entity Framework</span><span class="sxs-lookup"><span data-stu-id="1300d-116">How to: Create a Data Service Using an ADO.NET Entity Framework Data Source</span></span>](../../../../docs/framework/data/wcf/create-a-data-service-using-an-adonet-ef-data-wcf.md)
