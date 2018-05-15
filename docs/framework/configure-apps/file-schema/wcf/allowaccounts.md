---
title: '&lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: bbfe0d5d531cf61c01f95d0e82ce0f894031d6f3
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltallowaccountsgt"></a><span data-ttu-id="08b65-102">&lt;allowAccounts&gt;</span><span class="sxs-lookup"><span data-stu-id="08b65-102">&lt;allowAccounts&gt;</span></span>
<span data-ttu-id="08b65-103">Contient une collection d’éléments de configuration qui spécifient l’utilisateur des comptes pour les processus qui hébergent les services Windows Communication Foundation (WCF) et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="08b65-103">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="08b65-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="08b65-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08b65-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08b65-105">Syntax</span></span>  
  
```xml  
<allowAccounts>  
   <add securityIdentifier="String"/>  
</allowAccounts>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="08b65-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="08b65-106">Attributes and Elements</span></span>  
 <span data-ttu-id="08b65-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="08b65-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="08b65-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="08b65-108">Attributes</span></span>  
 <span data-ttu-id="08b65-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="08b65-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="08b65-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="08b65-110">Child Elements</span></span>  
  
|<span data-ttu-id="08b65-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="08b65-111">Attribute</span></span>|<span data-ttu-id="08b65-112">Description</span><span class="sxs-lookup"><span data-stu-id="08b65-112">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="08b65-113">\<add></span><span class="sxs-lookup"><span data-stu-id="08b65-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="08b65-114">Ajoute un compte d'utilisateur pour les processus qui hébergent des services [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] et qui disposent d'un accès de connexion au service de partage</span><span class="sxs-lookup"><span data-stu-id="08b65-114">Adds a user account for processes that host [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="08b65-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="08b65-115">Parent Elements</span></span>  
  
|<span data-ttu-id="08b65-116">Élément</span><span class="sxs-lookup"><span data-stu-id="08b65-116">Element</span></span>|<span data-ttu-id="08b65-117">Description</span><span class="sxs-lookup"><span data-stu-id="08b65-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="08b65-118">[\<NET.PIPE >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) ou [ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="08b65-118">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="08b65-119">Spécifie les paramètres de configuration pour le canal du réseau ou les services de partage TCP.</span><span class="sxs-lookup"><span data-stu-id="08b65-119">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="08b65-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08b65-120">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
