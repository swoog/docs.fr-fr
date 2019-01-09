---
title: '&lt;NET.pipe&gt;'
ms.date: 03/30/2017
ms.assetid: 6a0f0318-f8f6-466c-9fae-199d7274a82e
ms.openlocfilehash: 8a525f0684902841a2be75823932935e7533ba8b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151148"
---
# <a name="ltnetpipegt"></a><span data-ttu-id="e0203-102">&lt;NET.pipe&gt;</span><span class="sxs-lookup"><span data-stu-id="e0203-102">&lt;net.pipe&gt;</span></span>
<span data-ttu-id="e0203-103">Spécifie les paramètres de configuration du service d'activation du canal nommé, qui gère la durée de vie de la connexion du canal nommé et les demandes d'activation qui arrivent par des canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="e0203-103">Specifies configuration settings for the Named Pipe Activation Service, which manages the lifetime of the named pipe connection, and handles activation requests that arrive over named pipes.</span></span>  
  
 <span data-ttu-id="e0203-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="e0203-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="e0203-105">\<NET.PIPE ></span><span class="sxs-lookup"><span data-stu-id="e0203-105">\<net.pipe></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0203-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0203-106">Syntax</span></span>  
  
```xml  
<configuration>
  <system.serviceModel.activation>
    <net.pipe maxPendingAccepts="Integer"
              maxPendingConnections="Integer"
              receiveTimeout="TimeSpan">
      <allowAccounts>
        <!-- LocalSystem account -->
        <add securityIdentifier="S-1-5-18" />
        <!-- LocalService account -->
        <add securityIdentifier="S-1-5-19" />
        <!-- Administrators account -->
        <add securityIdentifier="S-1-5-20" />
        <!-- Network Service account -->
        <add securityIdentifier="S-1-5-32-544" />
        <!-- IIS_IUSRS account (Vista only) -->
        <add securityIdentifier="S-1-5-32-568" />
      </allowAccounts>
    </net.pipe>
  </system.serviceModel.activation>
</configuration>
```  
  
## <a name="type"></a><span data-ttu-id="e0203-107">Type</span><span class="sxs-lookup"><span data-stu-id="e0203-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e0203-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e0203-108">Attributes and Elements</span></span>  
 <span data-ttu-id="e0203-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e0203-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e0203-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="e0203-110">Attributes</span></span>  
  
|<span data-ttu-id="e0203-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0203-111">Attribute</span></span>|<span data-ttu-id="e0203-112">Description</span><span class="sxs-lookup"><span data-stu-id="e0203-112">Description</span></span>|  
|---------------|-----------------|  
|`maxPendingAccepts`|<span data-ttu-id="e0203-113">Entier qui spécifie le nombre maximal de threads d'acceptation simultanés en attente sur le point de terminaison d'écoute du service de partage.</span><span class="sxs-lookup"><span data-stu-id="e0203-113">An integer that specifies the maximum outstanding concurrent accepting threads on the listening endpoint for the sharing service.</span></span> <span data-ttu-id="e0203-114">La valeur par défaut est 2.</span><span class="sxs-lookup"><span data-stu-id="e0203-114">The default is 2.</span></span>|  
|`maxPendingConnections`|<span data-ttu-id="e0203-115">Entier qui définit le nombre maximal de connexions qui peuvent attendre la distribution.</span><span class="sxs-lookup"><span data-stu-id="e0203-115">An integer that specifies the maximum number of connections that can wait for dispatch.</span></span> <span data-ttu-id="e0203-116">La valeur par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="e0203-116">The default is 100.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="e0203-117">`TimeSpan` qui spécifie le délai d'attente pour lire les données d'encadrement et effectuer la distribution de la connexion à partir des connexions sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="e0203-117">A `TimeSpan` that specifies the timeout for reading the framing data and performing connection dispatching from the underlining connections.</span></span> <span data-ttu-id="e0203-118">La valeur par défaut est « 00:00:10 ».</span><span class="sxs-lookup"><span data-stu-id="e0203-118">The default is "00:00:10"</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e0203-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e0203-119">Child Elements</span></span>  
  
|<span data-ttu-id="e0203-120">Élément</span><span class="sxs-lookup"><span data-stu-id="e0203-120">Element</span></span>|<span data-ttu-id="e0203-121">Description</span><span class="sxs-lookup"><span data-stu-id="e0203-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0203-122">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="e0203-122">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="e0203-123">Une collection d’éléments de configuration qui contiennent un `securityIdentifier` attribut pour spécifier les comptes d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="e0203-123">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e0203-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e0203-124">Parent Elements</span></span>  
  
|<span data-ttu-id="e0203-125">Élément</span><span class="sxs-lookup"><span data-stu-id="e0203-125">Element</span></span>|<span data-ttu-id="e0203-126">Description</span><span class="sxs-lookup"><span data-stu-id="e0203-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e0203-127">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="e0203-127">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="e0203-128">Contient les paramètres de configuration du processus de l'écouteur SMSvcHost.exe.</span><span class="sxs-lookup"><span data-stu-id="e0203-128">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e0203-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0203-129">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection>
