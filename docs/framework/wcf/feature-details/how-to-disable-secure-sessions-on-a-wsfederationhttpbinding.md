---
title: 'Comment : désactiver des sessions sécurisées sur une classe WSFederationHttpBinding'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, federation
- federation
ms.assetid: 675fa143-6a4e-4be3-8afc-673334ab55ec
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 97fc358ac66bb92ccc40c92207bf6561f61b84f6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33489874"
---
# <a name="how-to-disable-secure-sessions-on-a-wsfederationhttpbinding"></a><span data-ttu-id="3320a-102">Comment : désactiver des sessions sécurisées sur une classe WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="3320a-102">How to: Disable Secure Sessions on a WSFederationHttpBinding</span></span>
<span data-ttu-id="3320a-103">Certains services peuvent requérir des informations d'identification fédérées mais ne prennent pas en charge les sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="3320a-103">Some services may require federated credentials but not support secure sessions.</span></span> <span data-ttu-id="3320a-104">Dans ce cas, vous devez désactiver la fonctionnalité de session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3320a-104">In that case, you must disable the secure session feature.</span></span> <span data-ttu-id="3320a-105">Contrairement à la <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`>, le <xref:System.ServiceModel.WSFederationHttpBinding> classe ne fournit pas la possibilité de désactiver des sessions sécurisées lors de la communication avec un service.</span><span class="sxs-lookup"><span data-stu-id="3320a-105">Unlike the <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`>, the <xref:System.ServiceModel.WSFederationHttpBinding> class does not provide a way to disable secure sessions when communicating with a service.</span></span> <span data-ttu-id="3320a-106">À la place, vous devez créer une liaison personnalisée qui remplace les paramètres de session sécurisée par un démarrage.</span><span class="sxs-lookup"><span data-stu-id="3320a-106">Instead, you must create a custom binding that replaces the secure session settings with a bootstrap.</span></span>  
  
 <span data-ttu-id="3320a-107">Cette rubrique montre comment modifier les éléments de liaison contenus dans une <xref:System.ServiceModel.WSFederationHttpBinding> pour créer une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3320a-107">This topic demonstrates how to modify the binding elements contained within a <xref:System.ServiceModel.WSFederationHttpBinding> to create a custom binding.</span></span> <span data-ttu-id="3320a-108">Le résultat est identique à <xref:System.ServiceModel.WSFederationHttpBinding> mais n'utilise pas de sessions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="3320a-108">The result is identical to the <xref:System.ServiceModel.WSFederationHttpBinding> except that it does not use secure sessions.</span></span>  
  
### <a name="to-create-a-custom-federated-binding-without-secure-session"></a><span data-ttu-id="3320a-109">Pour créer une liaison fédérée personnalisée sans session sécurisée</span><span class="sxs-lookup"><span data-stu-id="3320a-109">To create a custom federated binding without secure session</span></span>  
  
1.  <span data-ttu-id="3320a-110">Créez une instance de la classe <xref:System.ServiceModel.WSFederationHttpBinding> soit impérativement dans du code, soit en la chargeant à partir du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="3320a-110">Create an instance of the <xref:System.ServiceModel.WSFederationHttpBinding> class either imperatively in code or by loading one from the configuration file.</span></span>  
  
2.  <span data-ttu-id="3320a-111">Clonez la <xref:System.ServiceModel.WSFederationHttpBinding> dans une <xref:System.ServiceModel.Channels.CustomBinding>.</span><span class="sxs-lookup"><span data-stu-id="3320a-111">Clone the <xref:System.ServiceModel.WSFederationHttpBinding> into a <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
3.  <span data-ttu-id="3320a-112">Recherchez <xref:System.ServiceModel.Channels.SecurityBindingElement> dans <xref:System.ServiceModel.Channels.CustomBinding>.</span><span class="sxs-lookup"><span data-stu-id="3320a-112">Find the <xref:System.ServiceModel.Channels.SecurityBindingElement> in the <xref:System.ServiceModel.Channels.CustomBinding>.</span></span>  
  
4.  <span data-ttu-id="3320a-113">Recherchez <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> dans <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span><span class="sxs-lookup"><span data-stu-id="3320a-113">Find the <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters> in the <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span></span>  
  
5.  <span data-ttu-id="3320a-114">Remplacez le <xref:System.ServiceModel.Channels.SecurityBindingElement> d'origine par l'élément de liaison de sécurité de démarrage des <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters>.</span><span class="sxs-lookup"><span data-stu-id="3320a-114">Replace the original <xref:System.ServiceModel.Channels.SecurityBindingElement> with the bootstrap security binding element from the <xref:System.ServiceModel.Security.Tokens.SecureConversationSecurityTokenParameters>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3320a-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="3320a-115">Example</span></span>  
 <span data-ttu-id="3320a-116">L’exemple suivant permet de créer une liaison fédérée personnalisée sans session sécurisée.</span><span class="sxs-lookup"><span data-stu-id="3320a-116">This following example creates a custom federated binding without secure session.</span></span>  
  
 [!code-csharp[c_CustomFederationBinding#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_customfederationbinding/cs/c_customfederationbinding.cs#0)]
 [!code-vb[c_CustomFederationBinding#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_customfederationbinding/vb/c_customfederationbinding.vb#0)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3320a-117">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="3320a-117">Compiling the Code</span></span>  
  
-   <span data-ttu-id="3320a-118">Pour compiler l'exemple de code, créez un projet qui référence l'assembly System.ServiceModel.dll.</span><span class="sxs-lookup"><span data-stu-id="3320a-118">To compile the code example, create a project that references the System.ServiceModel.dll assembly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3320a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3320a-119">See Also</span></span>  
 [<span data-ttu-id="3320a-120">Liaisons et sécurité</span><span class="sxs-lookup"><span data-stu-id="3320a-120">Bindings and Security</span></span>](../../../../docs/framework/wcf/feature-details/bindings-and-security.md)
