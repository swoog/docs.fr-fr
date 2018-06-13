---
title: '&lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: 097112a8b54467843554047882e55b62d7813c0c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33352875"
---
# <a name="ltallowaccountsgt"></a><span data-ttu-id="243f9-102">&lt;allowAccounts&gt;</span><span class="sxs-lookup"><span data-stu-id="243f9-102">&lt;allowAccounts&gt;</span></span>
<span data-ttu-id="243f9-103">Contient une collection d’éléments de configuration qui spécifient l’utilisateur des comptes pour les processus qui hébergent les services Windows Communication Foundation (WCF) et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="243f9-103">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="243f9-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="243f9-104">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="243f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="243f9-105">Syntax</span></span>  
  
```xml  
<allowAccounts>  
   <add securityIdentifier="String"/>  
</allowAccounts>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="243f9-106">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="243f9-106">Attributes and Elements</span></span>  
 <span data-ttu-id="243f9-107">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="243f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="243f9-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="243f9-108">Attributes</span></span>  
 <span data-ttu-id="243f9-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="243f9-109">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="243f9-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="243f9-110">Child Elements</span></span>  
  
|<span data-ttu-id="243f9-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="243f9-111">Attribute</span></span>|<span data-ttu-id="243f9-112">Description</span><span class="sxs-lookup"><span data-stu-id="243f9-112">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="243f9-113">\<add></span><span class="sxs-lookup"><span data-stu-id="243f9-113">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="243f9-114">Ajoute un compte d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage</span><span class="sxs-lookup"><span data-stu-id="243f9-114">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="243f9-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="243f9-115">Parent Elements</span></span>  
  
|<span data-ttu-id="243f9-116">Élément</span><span class="sxs-lookup"><span data-stu-id="243f9-116">Element</span></span>|<span data-ttu-id="243f9-117">Description</span><span class="sxs-lookup"><span data-stu-id="243f9-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="243f9-118">[\<NET.PIPE >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) ou [ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="243f9-118">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="243f9-119">Spécifie les paramètres de configuration pour le canal du réseau ou les services de partage TCP.</span><span class="sxs-lookup"><span data-stu-id="243f9-119">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="243f9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="243f9-120">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
