---
title: <allowAccounts>
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: fd3121146577122446ba82528fc6e46dadbf5033
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255547"
---
# <a name="allowaccounts"></a><span data-ttu-id="0c8b1-101">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="0c8b1-101">\<allowAccounts></span></span>
<span data-ttu-id="0c8b1-102">Contient une collection d’éléments de configuration qui spécifient l’utilisateur des comptes pour les processus qui hébergent les services Windows Communication Foundation (WCF) et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="0c8b1-102">Contains a collection of configuration elements that specify user accounts for processes that host Windows Communication Foundation (WCF) services, and are granted connection access to the sharing service.</span></span>  
  
 <span data-ttu-id="0c8b1-103">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="0c8b1-103">\<system.serviceModel.activation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c8b1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c8b1-104">Syntax</span></span>  
  
```xml  
<allowAccounts>
  <add securityIdentifier="String" />
</allowAccounts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c8b1-105">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0c8b1-105">Attributes and Elements</span></span>  
 <span data-ttu-id="0c8b1-106">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0c8b1-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0c8b1-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c8b1-107">Attributes</span></span>  
 <span data-ttu-id="0c8b1-108">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0c8b1-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0c8b1-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c8b1-109">Child Elements</span></span>  
  
|<span data-ttu-id="0c8b1-110">Attribut</span><span class="sxs-lookup"><span data-stu-id="0c8b1-110">Attribute</span></span>|<span data-ttu-id="0c8b1-111">Description</span><span class="sxs-lookup"><span data-stu-id="0c8b1-111">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="0c8b1-112">\<add></span><span class="sxs-lookup"><span data-stu-id="0c8b1-112">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|<span data-ttu-id="0c8b1-113">Ajoute un compte d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage</span><span class="sxs-lookup"><span data-stu-id="0c8b1-113">Adds a user account for processes that host WCF services, and are granted connection access to the sharing service</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0c8b1-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0c8b1-114">Parent Elements</span></span>  
  
|<span data-ttu-id="0c8b1-115">Élément</span><span class="sxs-lookup"><span data-stu-id="0c8b1-115">Element</span></span>|<span data-ttu-id="0c8b1-116">Description</span><span class="sxs-lookup"><span data-stu-id="0c8b1-116">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0c8b1-117">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span><span class="sxs-lookup"><span data-stu-id="0c8b1-117">[\<net.pipe>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) or [\<net.tcp>](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)</span></span>|<span data-ttu-id="0c8b1-118">Spécifie les paramètres de configuration pour le canal du réseau ou les services de partage TCP.</span><span class="sxs-lookup"><span data-stu-id="0c8b1-118">Specifies configuration settings for the Net Pipe or TCP sharing services.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0c8b1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c8b1-119">See also</span></span>
- <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>
- <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
