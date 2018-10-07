---
title: '&lt;net.tcp&gt;'
ms.date: 03/30/2017
ms.assetid: 8bc2f2be-11c1-4bab-9018-1d21ae568d94
ms.openlocfilehash: c67aeca183eb476460fa0be2c6dcd9c6077165d8
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48842344"
---
# <a name="ltnettcpgt"></a><span data-ttu-id="79d25-102">&lt;net.tcp&gt;</span><span class="sxs-lookup"><span data-stu-id="79d25-102">&lt;net.tcp&gt;</span></span>
<span data-ttu-id="79d25-103">Spécifie les paramètres de configuration du service de partage de port NET.TCP, qui permet à plusieurs processus de partager le même port TCP.</span><span class="sxs-lookup"><span data-stu-id="79d25-103">Specifies configuration settings for the NET.TCP Port Sharing Service, which allows multiple processes to share the same TCP port.</span></span>  
  
 <span data-ttu-id="79d25-104">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="79d25-104">\<system.serviceModel.activation></span></span>  
<span data-ttu-id="79d25-105">\<net.tcp></span><span class="sxs-lookup"><span data-stu-id="79d25-105">\<net.tcp></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79d25-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79d25-106">Syntax</span></span>  
  
```xml  
<configuration>  
   <system.serviceModel.activation>  
       <net.tcp listenBacklog="Integer"  
          maxPendingAccepts="Integer"  
          maxPendingConnections="Integer"  
          receiveTimeout="TimeSpan"  
          teredoEnabled="Boolean">  
          <allowAccounts>  
             <!-- LocalSystem account -->   
             <add securityIdentifier="S-1-5-18"/>  
             <!-- LocalService account -->   
             <add securityIdentifier="S-1-5-19"/>  
             <!-- Administrators account -->   
             <add securityIdentifier="S-1-5-20"/>  
             <!-- Network Service account -->   
             <add securityIdentifier="S-1-5-32-544" />  
             <!-- IIS_IUSRS account (Vista only)-->   
             <add securityIdentifier="S-1-5-32-568"/>  
           </allowAccounts>  
       </net.tcp>  
   </system.serviceModel.activation>  
</configuration>  
```  
  
## <a name="type"></a><span data-ttu-id="79d25-107">Type</span><span class="sxs-lookup"><span data-stu-id="79d25-107">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="79d25-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="79d25-108">Attributes and Elements</span></span>  
 <span data-ttu-id="79d25-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="79d25-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="79d25-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="79d25-110">Attributes</span></span>  
  
|<span data-ttu-id="79d25-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="79d25-111">Attribute</span></span>|<span data-ttu-id="79d25-112">Description</span><span class="sxs-lookup"><span data-stu-id="79d25-112">Description</span></span>|  
|---------------|-----------------|  
|`listenBacklog`|<span data-ttu-id="79d25-113">Entier qui spécifie le nombre maximal de connexions en attente qui est accepté à partir de la connexion partagée, mais n’est pas encore distribué aux services Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="79d25-113">An integer that specifies the maximum outstanding connections that are accepted from the shared connection, but are not yet dispatched to Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="79d25-114">La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="79d25-114">The default is 10.</span></span>|  
|`maxPendingAccepts`|<span data-ttu-id="79d25-115">Entier qui spécifie le nombre maximal de threads d'acceptation simultanés en attente sur le point de terminaison d'écoute du service de partage.</span><span class="sxs-lookup"><span data-stu-id="79d25-115">An integer that specifies the maximum outstanding concurrent accepting threads on the listening endpoint for the sharing service.</span></span> <span data-ttu-id="79d25-116">La valeur par défaut est 2.</span><span class="sxs-lookup"><span data-stu-id="79d25-116">The default is 2.</span></span>|  
|`MaxPendingConnections`|<span data-ttu-id="79d25-117">Nombre maximal de connexions que l'écouteur peut mettre en attente d'acceptation par l'application.</span><span class="sxs-lookup"><span data-stu-id="79d25-117">The maximum number of connections that the listener can have waiting to be accepted by the application.</span></span> <span data-ttu-id="79d25-118">Lorsque cette valeur de quota est dépassée, les nouvelles connexions entrantes sont supprimées plutôt que mises en attente d'acceptation.</span><span class="sxs-lookup"><span data-stu-id="79d25-118">When this quota value is exceeded, new incoming connections are dropped rather than waiting to be accepted.</span></span> <span data-ttu-id="79d25-119">Les fonctionnalités de connexion telles que la sécurité des messages peuvent entraîner qu'un client ouvre plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="79d25-119">Connection features such as message security can cause a client to open more than one connection.</span></span> <span data-ttu-id="79d25-120">Les administrateurs de service doivent prendre en compte ces connexions supplémentaires lors de la définition de cette valeur de quota.</span><span class="sxs-lookup"><span data-stu-id="79d25-120">Service administrators should account for these additional connections when setting this quota value.</span></span> <span data-ttu-id="79d25-121">La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="79d25-121">The default is 10.</span></span>|  
|`receiveTimeout`|<span data-ttu-id="79d25-122">`TimeSpan` qui spécifie le délai d'attente pour lire les données d'encadrement et effectuer la distribution de la connexion à partir des connexions sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="79d25-122">A `TimeSpan` that specifies the timeout for reading the framing data and performing connection dispatching from the underlining connections.</span></span> <span data-ttu-id="79d25-123">La valeur par défaut est « 00:00:10 ».</span><span class="sxs-lookup"><span data-stu-id="79d25-123">The default is "00:00:10".</span></span>|  
|`teredoEnabled`|<span data-ttu-id="79d25-124">Valeur booléenne qui indique si le service de partage de port utilise le service Microsoft Teredo pour écouter les ports TCP pour le compte de services WCF.</span><span class="sxs-lookup"><span data-stu-id="79d25-124">A Boolean value that indicates whether the port sharing service uses Microsoft Teredo service to listen on TCP ports on behalf of WCF services.</span></span> <span data-ttu-id="79d25-125">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="79d25-125">The default is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="79d25-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="79d25-126">Child Elements</span></span>  
  
|<span data-ttu-id="79d25-127">Élément</span><span class="sxs-lookup"><span data-stu-id="79d25-127">Element</span></span>|<span data-ttu-id="79d25-128">Description</span><span class="sxs-lookup"><span data-stu-id="79d25-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="79d25-129">\<allowAccounts></span><span class="sxs-lookup"><span data-stu-id="79d25-129">\<allowAccounts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/allowaccounts.md)|<span data-ttu-id="79d25-130">Une collection d’éléments de configuration qui contiennent un `securityIdentifier` attribut pour spécifier les comptes d’utilisateur pour les processus qui hébergent des services WCF et qui disposent d’accès à la connexion au service de partage.</span><span class="sxs-lookup"><span data-stu-id="79d25-130">A collection of configuration elements that contain a `securityIdentifier` attribute to specify user accounts for processes that host WCF services, and are granted connection access to the sharing service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="79d25-131">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="79d25-131">Parent Elements</span></span>  
  
|<span data-ttu-id="79d25-132">Élément</span><span class="sxs-lookup"><span data-stu-id="79d25-132">Element</span></span>|<span data-ttu-id="79d25-133">Description</span><span class="sxs-lookup"><span data-stu-id="79d25-133">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="79d25-134">\<system.serviceModel.activation></span><span class="sxs-lookup"><span data-stu-id="79d25-134">\<system.serviceModel.activation></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel-activation.md)|<span data-ttu-id="79d25-135">Contient les paramètres de configuration du processus de l'écouteur SMSvcHost.exe.</span><span class="sxs-lookup"><span data-stu-id="79d25-135">Contains configuration settings for the listener process SMSvcHost.exe.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="79d25-136">Notes</span><span class="sxs-lookup"><span data-stu-id="79d25-136">Remarks</span></span>  
 <span data-ttu-id="79d25-137">Pour plus d’informations sur le partage de port, consultez [le partage de ports Net.TCP](../../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="79d25-137">For more information on port sharing, see [Net.TCP Port Sharing](../../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md).</span></span> <span data-ttu-id="79d25-138">Pour comprendre comment configurer le service de partage de ports, consultez [configurer le Service de partage de Port Net.TCP](../../../../../docs/framework/wcf/feature-details/configuring-the-net-tcp-port-sharing-service.md).</span><span class="sxs-lookup"><span data-stu-id="79d25-138">To understand how to configure the port sharing service, see [Configuring the Net.TCP Port Sharing Service](../../../../../docs/framework/wcf/feature-details/configuring-the-net-tcp-port-sharing-service.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79d25-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79d25-139">See Also</span></span>  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection>  
 [<span data-ttu-id="79d25-140">Partage de ports Net.TCP</span><span class="sxs-lookup"><span data-stu-id="79d25-140">Net.TCP Port Sharing</span></span>](../../../../../docs/framework/wcf/feature-details/net-tcp-port-sharing.md)  
 [<span data-ttu-id="79d25-141">Configuration du service de partage de ports Net.TCP</span><span class="sxs-lookup"><span data-stu-id="79d25-141">Configuring the Net.TCP Port Sharing Service</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-the-net-tcp-port-sharing-service.md)
