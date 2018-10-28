---
title: "Comment : créer un SecurityBindingElement pour un mode d'authentification spécifié"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a7c7747a-5b8c-463f-8493-7266dac75066
ms.openlocfilehash: afc89d14623a25dbaa1ac5c9a58e11dd3e963617
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/26/2018
ms.locfileid: "50088674"
---
# <a name="how-to-create-a-securitybindingelement-for-a-specified-authentication-mode"></a><span data-ttu-id="5f182-102">Comment : créer un SecurityBindingElement pour un mode d'authentification spécifié</span><span class="sxs-lookup"><span data-stu-id="5f182-102">How to: Create a SecurityBindingElement for a Specified Authentication Mode</span></span>
<span data-ttu-id="5f182-103">Windows Communication Foundation (WCF) fournit plusieurs modes par lequel les clients et les services de s’authentifier entre eux.</span><span class="sxs-lookup"><span data-stu-id="5f182-103">Windows Communication Foundation (WCF) provides several modes by which clients and services authenticate to one another.</span></span> <span data-ttu-id="5f182-104">Vous pouvez créer des éléments de liaison de sécurité pour ces modes d’authentification en utilisant des méthodes statiques sur la classe <xref:System.ServiceModel.Channels.SecurityBindingElement> ou par la configuration, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="5f182-104">You can create security binding elements for these authentication modes by using static methods on the <xref:System.ServiceModel.Channels.SecurityBindingElement> class or through configuration, as shown in the following example.</span></span>  
  
 <span data-ttu-id="5f182-105">Pour plus d’informations sur les 18 modes d’authentification, consultez [Modes d’authentification SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md).</span><span class="sxs-lookup"><span data-stu-id="5f182-105">For more information about the 18 authentication modes, see [SecurityBindingElement Authentication Modes](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f182-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="5f182-106">Example</span></span>  
 <span data-ttu-id="5f182-107">L’exemple de code suivant présente des méthodes pour créer des liaisons pour les divers modes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="5f182-107">The following code example shows methods for creating bindings for the various authentication modes.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5f182-108">Une fois qu'une instance de l'objet <xref:System.ServiceModel.Channels.SecurityBindingElement> est créée, plusieurs propriétés sont immuables, telles que <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.KeyType%2A> et <xref:System.ServiceModel.Channels.SecurityBindingElement.MessageSecurityVersion%2A>.</span><span class="sxs-lookup"><span data-stu-id="5f182-108">Once an instance of the <xref:System.ServiceModel.Channels.SecurityBindingElement> object is created, a number of properties are immutable, such as <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.KeyType%2A> and <xref:System.ServiceModel.Channels.SecurityBindingElement.MessageSecurityVersion%2A>.</span></span> <span data-ttu-id="5f182-109">L'appel de `set` sur de telles propriétés ne les modifie pas.</span><span class="sxs-lookup"><span data-stu-id="5f182-109">Calling `set` on such properties does not change them.</span></span>  
  
 [!code-csharp[c_CustomBindingsAuthMode#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombindingsauthmode/cs/source.cs#2)]
 [!code-vb[c_CustomBindingsAuthMode#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_custombindingsauthmode/vb/source.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="5f182-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f182-110">See Also</span></span>  
 [<span data-ttu-id="5f182-111">Modes d’authentification SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="5f182-111">SecurityBindingElement Authentication Modes</span></span>](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md)  
 [<span data-ttu-id="5f182-112">Guide pratique pour créer une liaison personnalisée à l’aide de SecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="5f182-112">How to: Create a Custom Binding Using the SecurityBindingElement</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
