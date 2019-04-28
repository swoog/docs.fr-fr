---
title: 'Procédure : Intercepter les Messages de Service de données (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing
- query interceptors [WCF Data Services]
ms.assetid: 24b9df1b-b54b-4795-a033-edf333675de6
ms.openlocfilehash: ad0673f72b1a81d6bcfaf0704ccd698eda7bb20c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61936511"
---
# <a name="how-to-intercept-data-service-messages-wcf-data-services"></a><span data-ttu-id="b9344-102">Procédure : Intercepter les Messages de Service de données (WCF Data Services)</span><span class="sxs-lookup"><span data-stu-id="b9344-102">How to: Intercept Data Service Messages (WCF Data Services)</span></span>
<span data-ttu-id="b9344-103">Avec [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)], vous pouvez intercepter des messages de demande afin de pouvoir ajouter la logique personnalisée à une opération.</span><span class="sxs-lookup"><span data-stu-id="b9344-103">With [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)], you can intercept request messages so that you can add custom logic to an operation.</span></span> <span data-ttu-id="b9344-104">Pour intercepter un message, vous utilisez les méthodes attribuées spécialement dans le service de données.</span><span class="sxs-lookup"><span data-stu-id="b9344-104">To intercept a message, you use specially attributed methods in the data service.</span></span> <span data-ttu-id="b9344-105">Pour plus d’informations, consultez [intercepteurs](../../../../docs/framework/data/wcf/interceptors-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="b9344-105">For more information, see [Interceptors](../../../../docs/framework/data/wcf/interceptors-wcf-data-services.md).</span></span>  
  
 <span data-ttu-id="b9344-106">L'exemple de cette rubrique utilise l'exemple du service de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="b9344-106">The example in this topic uses the Northwind sample data service.</span></span> <span data-ttu-id="b9344-107">Ce service est créé lorsque vous effectuez la [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="b9344-107">This service is created when you complete the [WCF Data Services quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span></span>  
  
### <a name="to-define-a-query-interceptor-for-the-orders-entity-set"></a><span data-ttu-id="b9344-108">Pour définir un intercepteur de requête pour le jeu d'entités Orders</span><span class="sxs-lookup"><span data-stu-id="b9344-108">To define a query interceptor for the Orders entity set</span></span>  
  
1. <span data-ttu-id="b9344-109">Dans le projet de service de données Northwind, ouvrez le fichier Northwind.svc.</span><span class="sxs-lookup"><span data-stu-id="b9344-109">In the Northwind data service project, open the Northwind.svc file.</span></span>  
  
2. <span data-ttu-id="b9344-110">Dans la page de codes de la classe `Northwind`, ajoutez l'instruction suivante `using` (`Imports` en Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="b9344-110">In the code page for the `Northwind` class, add the following `using` statement (`Imports` in Visual Basic).</span></span>  
  
     [!code-csharp[Astoria Northwind Service#UsingLinqExpressions](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#usinglinqexpressions)]
     [!code-vb[Astoria Northwind Service#UsingLinqExpressions](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#usinglinqexpressions)]  
  
3. <span data-ttu-id="b9344-111">Dans la classe `Northwind`, définissez une méthode d'opération de service nommée `OnQueryOrders` comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9344-111">In the `Northwind` class, define a service operation method named `OnQueryOrders` as follows:</span></span>  
  
     [!code-csharp[Astoria Northwind Service#QueryInterceptorDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#queryinterceptordef)]
     [!code-vb[Astoria Northwind Service#QueryInterceptorDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#queryinterceptordef)]  
  
### <a name="to-define-a-change-interceptor-for-the-products-entity-set"></a><span data-ttu-id="b9344-112">Pour définir un intercepteur de modification pour le jeu d'entités Products</span><span class="sxs-lookup"><span data-stu-id="b9344-112">To define a change interceptor for the Products entity set</span></span>  
  
1. <span data-ttu-id="b9344-113">Dans le projet de service de données Northwind, ouvrez le fichier Northwind.svc.</span><span class="sxs-lookup"><span data-stu-id="b9344-113">In the Northwind data service project, open the Northwind.svc file.</span></span>  
  
2. <span data-ttu-id="b9344-114">Dans la classe `Northwind`, définissez une méthode d'opération de service nommée `OnChangeProducts` comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9344-114">In the `Northwind` class, define a service operation method named `OnChangeProducts` as follows:</span></span>  
  
     [!code-csharp[Astoria Northwind Service#ChangeInterceptorDef](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#changeinterceptordef)]
     [!code-vb[Astoria Northwind Service#ChangeInterceptorDef](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#changeinterceptordef)]  
  
## <a name="example"></a><span data-ttu-id="b9344-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9344-115">Example</span></span>  
 <span data-ttu-id="b9344-116">Cet exemple définit une méthode d'interception de requête pour le jeu d'entités `Orders` qui retourne une expression lambda.</span><span class="sxs-lookup"><span data-stu-id="b9344-116">This example defines a query interceptor method for the `Orders` entity set that returns a lambda expression.</span></span> <span data-ttu-id="b9344-117">Cette expression contient un délégué qui filtre le `Orders` demandé en fonction du `Customers` connexe qui a un nom de contact spécifique.</span><span class="sxs-lookup"><span data-stu-id="b9344-117">This expression contains a delegate that filters the requested `Orders` based on related `Customers` that have a specific contact name.</span></span> <span data-ttu-id="b9344-118">Le nom est déterminé ensuite selon l'utilisateur demandeur.</span><span class="sxs-lookup"><span data-stu-id="b9344-118">The name is in turn determined based on the requesting user.</span></span> <span data-ttu-id="b9344-119">Cet exemple suppose que le service de données est hébergé dans une application Web ASP.NET qui utilise WCF, et que l'authentification est activée.</span><span class="sxs-lookup"><span data-stu-id="b9344-119">This example assumes that the data service is hosted within an ASP.NET Web application that uses WCF, and that authentication is enabled.</span></span> <span data-ttu-id="b9344-120">La classe <xref:System.Web.HttpContext> est utilisée pour récupérer le principe de la demande actuelle.</span><span class="sxs-lookup"><span data-stu-id="b9344-120">The <xref:System.Web.HttpContext> class is used to retrieve the principle of the current request.</span></span>  
  
 [!code-csharp[Astoria Northwind Service#QueryInterceptor](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#queryinterceptor)]
 [!code-vb[Astoria Northwind Service#QueryInterceptor](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#queryinterceptor)]  
  
## <a name="example"></a><span data-ttu-id="b9344-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9344-121">Example</span></span>  
 <span data-ttu-id="b9344-122">Cet exemple définit une méthode d'interception de modification pour le jeu d'entités `Products`.</span><span class="sxs-lookup"><span data-stu-id="b9344-122">This example defines a change interceptor method for the `Products` entity set.</span></span> <span data-ttu-id="b9344-123">Cette méthode valide l'entrée au service pour une opération <xref:System.Data.Services.UpdateOperations.Add> ou <xref:System.Data.Services.UpdateOperations.Change> et lève une exception si une modification est apportée à un produit de fin de série.</span><span class="sxs-lookup"><span data-stu-id="b9344-123">This method validates input to the service for an <xref:System.Data.Services.UpdateOperations.Add> or <xref:System.Data.Services.UpdateOperations.Change> operation and raises an exception if a change is being made to a discontinued product.</span></span> <span data-ttu-id="b9344-124">Elle bloque également la suppression de produits comme une opération non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b9344-124">It also blocks the deletion of products as an unsupported operation.</span></span>  
  
 [!code-csharp[Astoria Northwind Service#ChangeInterceptor](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria_northwind_service/cs/northwind2.svc.cs#changeinterceptor)]
 [!code-vb[Astoria Northwind Service#ChangeInterceptor](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria_northwind_service/vb/northwind2.svc.vb#changeinterceptor)]  
  
## <a name="see-also"></a><span data-ttu-id="b9344-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9344-125">See also</span></span>

- [<span data-ttu-id="b9344-126">Guide pratique pour Définir une opération de Service</span><span class="sxs-lookup"><span data-stu-id="b9344-126">How to: Define a Service Operation</span></span>](../../../../docs/framework/data/wcf/how-to-define-a-service-operation-wcf-data-services.md)
- [<span data-ttu-id="b9344-127">Définition de WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="b9344-127">Defining WCF Data Services</span></span>](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)
