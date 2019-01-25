---
title: 'Procédure : Créer un contrat Windows Communication Foundation avec une classe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1ad69393-3915-4e7f-9b91-b6fc59c6f5ba
ms.openlocfilehash: b32d4feb03daac33af8b7ca3b533a0b7013bb090
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54658924"
---
# <a name="how-to-create-a-windows-communication-foundation-contract-with-a-class"></a><span data-ttu-id="48ac9-102">Procédure : Créer un contrat Windows Communication Foundation avec une classe</span><span class="sxs-lookup"><span data-stu-id="48ac9-102">How to: Create a Windows Communication Foundation Contract with a Class</span></span>
<span data-ttu-id="48ac9-103">Le meilleur moyen de la création d’un contrat Windows Communication Foundation (WCF) est à l’aide d’une interface.</span><span class="sxs-lookup"><span data-stu-id="48ac9-103">The preferred way of creating a Windows Communication Foundation (WCF) contract is by using an interface.</span></span> <span data-ttu-id="48ac9-104">Pour plus d'informations, voir [Procédure : Définir un contrat de Service](../../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md).</span><span class="sxs-lookup"><span data-stu-id="48ac9-104">For more information, see [How to: Define a Service Contract](../../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md).</span></span> <span data-ttu-id="48ac9-105">Une autre solution, présentée dans cette rubrique, consiste à créer une classe, à appliquer l'attribut <xref:System.ServiceModel.ServiceContractAttribute> directement sur celle-ci, puis l'attribut <xref:System.ServiceModel.OperationContractAttribute> sur chacune des méthodes de la classe qui font partie du contrat.</span><span class="sxs-lookup"><span data-stu-id="48ac9-105">An alternative, outlined here, is to create a class and then apply the <xref:System.ServiceModel.ServiceContractAttribute> attribute to the class directly and the <xref:System.ServiceModel.OperationContractAttribute> attribute to each of the methods in the class that are part of the contract.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="48ac9-106">`[ServiceContract]` et `[ServiceContractAttribute]` produisent le même résultat.</span><span class="sxs-lookup"><span data-stu-id="48ac9-106">`[ServiceContract]` and `[ServiceContractAttribute]` do the same thing.</span></span> <span data-ttu-id="48ac9-107">La même chose vaut pour `[OperationContract]` et `[OperationContractAttribute]`.</span><span class="sxs-lookup"><span data-stu-id="48ac9-107">The same thing is true for `[OperationContract]` and `[OperationContractAttribute]`.</span></span> <span data-ttu-id="48ac9-108">Dans chaque cas, le précédent est abrégé pour cette dernière.</span><span class="sxs-lookup"><span data-stu-id="48ac9-108">In each case, the former is shorthand for the latter.</span></span>  
  
 <span data-ttu-id="48ac9-109">Pour plus d’informations sur les contrats de service, consultez [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md).</span><span class="sxs-lookup"><span data-stu-id="48ac9-109">For more information about service contracts, see [Designing Service Contracts](../../../../docs/framework/wcf/designing-service-contracts.md).</span></span>  
  
### <a name="creating-a-windows-communication-foundation-contract-with-a-class"></a><span data-ttu-id="48ac9-110">Création d'un contrat Windows Communication Foundation à l'aide d'une classe</span><span class="sxs-lookup"><span data-stu-id="48ac9-110">Creating a Windows Communication Foundation contract with a class</span></span>  
  
1.  <span data-ttu-id="48ac9-111">Créer une nouvelle classe à l’aide de Visual Basic, C#, ou n’importe quel autre langage common language runtime.</span><span class="sxs-lookup"><span data-stu-id="48ac9-111">Create a new class using Visual Basic, C#, or any other common language runtime language.</span></span>  
  
2.  <span data-ttu-id="48ac9-112">Appliquez la classe <xref:System.ServiceModel.ServiceContractAttribute> à la classe.</span><span class="sxs-lookup"><span data-stu-id="48ac9-112">Apply the <xref:System.ServiceModel.ServiceContractAttribute> class to the class.</span></span>  
  
3.  <span data-ttu-id="48ac9-113">Créez des méthodes dans la classe.</span><span class="sxs-lookup"><span data-stu-id="48ac9-113">Create methods in the class.</span></span>  
  
4.  <span data-ttu-id="48ac9-114">Appliquer le <xref:System.ServiceModel.OperationContractAttribute> classe pour chaque méthode qui doit être exposé en tant que partie du contrat WCF public.</span><span class="sxs-lookup"><span data-stu-id="48ac9-114">Apply the <xref:System.ServiceModel.OperationContractAttribute> class to each method that must be exposed as part of the public WCF contract.</span></span>  
  
## <a name="example"></a><span data-ttu-id="48ac9-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="48ac9-115">Example</span></span>  
 <span data-ttu-id="48ac9-116">L'exemple de code suivant présente une classe qui définit un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="48ac9-116">The following code example shows a class that defines a service contract.</span></span>  
  
 [!code-csharp[c_HowTo_CreateContractWithClass#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howto_createcontractwithclass/cs/source.cs#1)]
 [!code-vb[c_HowTo_CreateContractWithClass#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howto_createcontractwithclass/vb/source.vb#1)]  
  
 <span data-ttu-id="48ac9-117">Les méthodes auxquelles la classe <xref:System.ServiceModel.OperationContractAttribute> est appliquée utilisent un modèle de message demande-réponse par défaut.</span><span class="sxs-lookup"><span data-stu-id="48ac9-117">The methods that have the <xref:System.ServiceModel.OperationContractAttribute> class applied use a request-reply message pattern by default.</span></span> <span data-ttu-id="48ac9-118">Pour plus d’informations sur ce modèle de message, consultez [Comment : Créer un contrat demande-réponse](../../../../docs/framework/wcf/feature-details/how-to-create-a-request-reply-contract.md).</span><span class="sxs-lookup"><span data-stu-id="48ac9-118">For more information about this message pattern, see [How to: Create a Request-Reply Contract](../../../../docs/framework/wcf/feature-details/how-to-create-a-request-reply-contract.md).</span></span> <span data-ttu-id="48ac9-119">Vous pouvez également créer et utiliser d’autres modèles de message en définissant les propriétés de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="48ac9-119">You can also create and use other message patterns by setting properties of the attribute.</span></span> <span data-ttu-id="48ac9-120">Pour plus d'exemples, consultez [Procédure : Créer un contrat unidirectionnel](../../../../docs/framework/wcf/feature-details/how-to-create-a-one-way-contract.md) et [Comment : Créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).</span><span class="sxs-lookup"><span data-stu-id="48ac9-120">For more examples, see [How to: Create a One-Way Contract](../../../../docs/framework/wcf/feature-details/how-to-create-a-one-way-contract.md) and [How to: Create a Duplex Contract](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48ac9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48ac9-121">See also</span></span>
- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
