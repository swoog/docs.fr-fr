---
title: "Comment : autoriser des demandes de métadonnées au cours de l'autorisation"
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- allowing metadata requests while authorizing [WCF]
ms.assetid: 90cec34f-b619-452b-a056-8b1c0de49d05
caps.latest.revision: 9
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 6b0b331da49fca7be5106610e4b6f144220cc849
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-allow-metadata-requests-while-authorizing"></a><span data-ttu-id="41465-102">Comment : autoriser des demandes de métadonnées au cours de l'autorisation</span><span class="sxs-lookup"><span data-stu-id="41465-102">How To: Allow Metadata Requests While Authorizing</span></span>
<span data-ttu-id="41465-103">Pendant l'autorisation personnalisée, il peut être nécessaire d'autoriser le traitement d'une demande de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="41465-103">During custom authorization, it may be necessary to allow a request for metadata to be processed.</span></span> <span data-ttu-id="41465-104">La rubrique suivante présente les étapes de validation d'une telle demande.</span><span class="sxs-lookup"><span data-stu-id="41465-104">The following topic walks through the steps to validate such a request.</span></span>  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]<span data-ttu-id="41465-105"> [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] autorisation, consultez [autorisation](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).</span><span class="sxs-lookup"><span data-stu-id="41465-105"> [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] authorization, see [Authorization](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md).</span></span>  
  
### <a name="to-allow-metadata-requests-during-authorization"></a><span data-ttu-id="41465-106">Pour autoriser les demandes de métadonnées pendant l'autorisation</span><span class="sxs-lookup"><span data-stu-id="41465-106">To allow metadata requests during authorization</span></span>  
  
1.  <span data-ttu-id="41465-107">Créez une extension de la classe <xref:System.ServiceModel.ServiceAuthorizationManager>.</span><span class="sxs-lookup"><span data-stu-id="41465-107">Create an extension of the <xref:System.ServiceModel.ServiceAuthorizationManager> class.</span></span>  
  
2.  <span data-ttu-id="41465-108">Remplacez la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A>.</span><span class="sxs-lookup"><span data-stu-id="41465-108">Override the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> method.</span></span> <span data-ttu-id="41465-109">La méthode retourne la valeur `true` ou `false` selon que l'autorisation est accordée ou non.</span><span class="sxs-lookup"><span data-stu-id="41465-109">The method returns `true` or `false` depending on whether authorization is allowed.</span></span> <span data-ttu-id="41465-110">Les informations relatives à la procédure en cours se trouvent dans le <xref:System.ServiceModel.OperationContext> passé comme paramètre à la méthode.</span><span class="sxs-lookup"><span data-stu-id="41465-110">Information about the current procedure is found in the <xref:System.ServiceModel.OperationContext> passed as a parameter to the method.</span></span>  
  
3.  <span data-ttu-id="41465-111">Dans la substitution, vérifiez le nom de contrat, l'espace de noms et l'action comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="41465-111">In the override, check the contract name, namespace, and the action as shown in the following example.</span></span> <span data-ttu-id="41465-112">Si les conditions sont valides, retournez `true.`</span><span class="sxs-lookup"><span data-stu-id="41465-112">If the conditions are valid, then return `true.`</span></span>  
  
4.  <span data-ttu-id="41465-113">Utilisez le point d'extensibilité pour employer la classe.</span><span class="sxs-lookup"><span data-stu-id="41465-113">Use the extensibility point to employ the class.</span></span> <span data-ttu-id="41465-114">Pour plus d’informations, consultez [Comment : créer un gestionnaire d’autorisation personnalisé pour un Service](../../../../docs/framework/wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="41465-114">For more information, see [How to: Create a Custom Authorization Manager for a Service](../../../../docs/framework/wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="41465-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="41465-115">Example</span></span>  
 <span data-ttu-id="41465-116">L'exemple suivant illustre une substitution de la méthode <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A>.</span><span class="sxs-lookup"><span data-stu-id="41465-116">The following example shows an override of the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> method.</span></span>  
  
 [!code-csharp[C_HowtoCheckForMexRequestsInAuthorization#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtocheckformexrequestsinauthorization/cs/source.cs#1)]
 [!code-vb[C_HowtoCheckForMexRequestsInAuthorization#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtocheckformexrequestsinauthorization/vb/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="41465-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41465-117">See Also</span></span>  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
 [<span data-ttu-id="41465-118">Autorisation</span><span class="sxs-lookup"><span data-stu-id="41465-118">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
 [<span data-ttu-id="41465-119">Gestion des revendications et autorisation avec le modèle d’identité</span><span class="sxs-lookup"><span data-stu-id="41465-119">Managing Claims and Authorization with the Identity Model</span></span>](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
