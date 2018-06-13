---
title: 'Comment : définir une opération de service (services de données WCF)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Service Operations [WCF Data Services]
- WCF Data Services, service operations
ms.assetid: dfcd3cb1-2f07-4d0b-b16a-6b056c4f45fa
ms.openlocfilehash: 7d40011e701525912c4406d1ab35712ee21009da
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33360881"
---
# <a name="how-to-define-a-service-operation-wcf-data-services"></a><span data-ttu-id="c5867-102">Comment : définir une opération de service (services de données WCF)</span><span class="sxs-lookup"><span data-stu-id="c5867-102">How to: Define a Service Operation (WCF Data Services)</span></span>
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]<span data-ttu-id="c5867-103"> exposent des méthodes définies sur le serveur comme des opérations de service.</span><span class="sxs-lookup"><span data-stu-id="c5867-103"> expose methods that are defined on the server as service operations.</span></span> <span data-ttu-id="c5867-104">Opérations de service permettent à un service de données fournir l’accès via un URI à une méthode qui est définie sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c5867-104">Service operations allow a data service to provide access through a URI to a method that is defined on the server.</span></span> <span data-ttu-id="c5867-105">Pour définir une opération de service, appliquez le [`WebGet]` ou `[WebInvoke]` d’attribut à la méthode.</span><span class="sxs-lookup"><span data-stu-id="c5867-105">To define a service operation, apply the [`WebGet]` or `[WebInvoke]` attribute to the method.</span></span> <span data-ttu-id="c5867-106">Pour prendre en charge les opérateurs de requête, l’opération de service doit retourner un <xref:System.Linq.IQueryable%601> instance.</span><span class="sxs-lookup"><span data-stu-id="c5867-106">To support query operators, the service operation must return an <xref:System.Linq.IQueryable%601> instance.</span></span> <span data-ttu-id="c5867-107">Les opérations de service peuvent accéder à la source de données sous-jacente via la propriété <xref:System.Data.Services.DataService%601.CurrentDataSource%2A> sur <xref:System.Data.Services.DataService%601>.</span><span class="sxs-lookup"><span data-stu-id="c5867-107">Service operations may access the underlying data source through the <xref:System.Data.Services.DataService%601.CurrentDataSource%2A> property on the <xref:System.Data.Services.DataService%601>.</span></span> <span data-ttu-id="c5867-108">Pour plus d’informations, consultez [les opérations de Service](../../../../docs/framework/data/wcf/service-operations-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="c5867-108">For more information, see [Service Operations](../../../../docs/framework/data/wcf/service-operations-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="c5867-109">L'exemple dans cette rubrique définit une opération de service nommée `GetOrdersByCity` qui retourne une instance <xref:System.Linq.IQueryable%601> filtrée d'objets `Orders` et  `Order_Details` connexes.</span><span class="sxs-lookup"><span data-stu-id="c5867-109">The example in this topic defines a service operation named `GetOrdersByCity` that returns a filtered <xref:System.Linq.IQueryable%601> instance of `Orders` and related `Order_Details` objects.</span></span> <span data-ttu-id="c5867-110">L'exemple accède à l'instance <xref:System.Data.Objects.ObjectContext> qui est la source de données pour l'exemple de service de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="c5867-110">The example accesses the <xref:System.Data.Objects.ObjectContext> instance that is the data source for the Northwind sample data service.</span></span> <span data-ttu-id="c5867-111">Ce service est créé lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="c5867-111">This service is created when you complete the [WCF Data Services quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span></span>  
  
### <a name="to-define-a-service-operation-in-the-northwind-data-service"></a><span data-ttu-id="c5867-112">Pour définir une opération de service dans le service de données Northwind</span><span class="sxs-lookup"><span data-stu-id="c5867-112">To define a service operation in the Northwind data service</span></span>  
  
1.  <span data-ttu-id="c5867-113">Dans le projet de service de données Northwind, ouvrez le fichier Northwind.svc.</span><span class="sxs-lookup"><span data-stu-id="c5867-113">In the Northwind data service project, open the Northwind.svc file.</span></span>  
  
2.  <span data-ttu-id="c5867-114">Dans la classe `Northwind`, définissez une méthode d'opération de service nommée `GetOrdersByCity` comme suit :</span><span class="sxs-lookup"><span data-stu-id="c5867-114">In the `Northwind` class, define a service operation method named `GetOrdersByCity` as follows:</span></span>  
  
     [!code-csharp[Astoria Northwind Service#ServiceOperationDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind service/cs/northwind2.svc.cs#serviceoperationdef)]
     [!code-vb[Astoria Northwind Service#ServiceOperationDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind service/vb/northwind2.svc.vb#serviceoperationdef)]  
  
3.  <span data-ttu-id="c5867-115">Dans la méthode `InitializeService` de la classe `Northwind`, ajoutez le code suivant pour permettre l'accès à l'opération de service :</span><span class="sxs-lookup"><span data-stu-id="c5867-115">In the `InitializeService` method of the `Northwind` class, add the following code to enable access to the service operation:</span></span>  
  
     [!code-csharp[Astoria Northwind Service#ServiceOperationConfig](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind service/cs/northwind2.svc.cs#serviceoperationconfig)]
     [!code-vb[Astoria Northwind Service#ServiceOperationConfig](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind service/vb/northwind2.svc.vb#serviceoperationconfig)]  
  
### <a name="to-query-the-getordersbycity-service-operation"></a><span data-ttu-id="c5867-116">Pour interroger l'opération de service GetOrdersByCity</span><span class="sxs-lookup"><span data-stu-id="c5867-116">To query the GetOrdersByCity service operation</span></span>  
  
-   <span data-ttu-id="c5867-117">Dans un navigateur Web, entrez l'un des URI suivants pour appeler l'opération de service définie dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c5867-117">In a Web browser, enter one of the following URIs to invoke the service operation that is defined in the following example:</span></span>  
  
    -   `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'`  
  
    -   `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$top=2`  
  
    -   `http://localhost:12345/Northwind.svc/GetOrdersByCity?city='London'&$expand=Order_Details&$orderby=RequiredDate desc`  
  
## <a name="example"></a><span data-ttu-id="c5867-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="c5867-118">Example</span></span>  
 <span data-ttu-id="c5867-119">L'exemple suivant implémente une opération de service nommée `GetOrderByCity` sur le service de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="c5867-119">The following example implements a service operation named `GetOrderByCity` on the Northwind data service.</span></span> <span data-ttu-id="c5867-120">Cette opération utilise ADO.NET Entity Framework pour retourner un jeu d'objets `Orders` et `Order_Details` connexes comme une instance <xref:System.Linq.IQueryable%601> basée sur le nom de ville fourni.</span><span class="sxs-lookup"><span data-stu-id="c5867-120">This operation uses the ADO.NET Entity Framework to return a set of `Orders` and related `Order_Details` objects as an <xref:System.Linq.IQueryable%601> instance based on the provided city name.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c5867-121">Les opérateurs de requête sont pris en charge sur ce point de terminaison d'opération de service parce que la méthode retourne une instance <xref:System.Linq.IQueryable%601>.</span><span class="sxs-lookup"><span data-stu-id="c5867-121">Query operators are supported on this service operation endpoint because the method returns an <xref:System.Linq.IQueryable%601> instance.</span></span>  
  
 [!code-csharp[Astoria Northwind Service#ServiceOperation](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind service/cs/northwind2.svc.cs#serviceoperation)]
 [!code-vb[Astoria Northwind Service#ServiceOperation](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind service/vb/northwind2.svc.vb#serviceoperation)]  
  
## <a name="see-also"></a><span data-ttu-id="c5867-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5867-122">See Also</span></span>  
 [<span data-ttu-id="c5867-123">Définition de WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="c5867-123">Defining WCF Data Services</span></span>](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)
