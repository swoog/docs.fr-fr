---
title: <factorySettings>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 202aad17-1b8b-4c87-ad57-4ca5de18ed35
ms.openlocfilehash: d8e87799962638ac6514ebb31bbc9e209b39c98d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790167"
---
# <a name="factorysettings"></a><span data-ttu-id="0c3ca-101">\<factorySettings></span><span class="sxs-lookup"><span data-stu-id="0c3ca-101">\<factorySettings></span></span>
<span data-ttu-id="0c3ca-102">Spécifie les paramètres du cache de la fabrique de canaux.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-102">Specifies the settings of the channel factory cache.</span></span>  
  
<span data-ttu-id="0c3ca-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0c3ca-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="0c3ca-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="0c3ca-104">\<behaviors></span></span>  
<span data-ttu-id="0c3ca-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="0c3ca-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="0c3ca-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0c3ca-106">\<behavior></span></span>  
<span data-ttu-id="0c3ca-107">\<sendMessageChannelCache></span><span class="sxs-lookup"><span data-stu-id="0c3ca-107">\<sendMessageChannelCache></span></span>  
<span data-ttu-id="0c3ca-108">\<factorySettings></span><span class="sxs-lookup"><span data-stu-id="0c3ca-108">\<factorySettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c3ca-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c3ca-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <sendMessageChannelCache allowUnsafeCaching="Boolean" >
        <factorySettings idleTimeout="TimeSpan" 
                         leaseTimeout="TimeSpan" 
                         maxItemsInCache="Integer" />
      </sendMessageChannelCache>
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c3ca-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0c3ca-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0c3ca-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0c3ca-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c3ca-112">Attributes</span></span>  
  
|<span data-ttu-id="0c3ca-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0c3ca-113">Attribute</span></span>|<span data-ttu-id="0c3ca-114">Description</span><span class="sxs-lookup"><span data-stu-id="0c3ca-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0c3ca-115">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="0c3ca-115">idleTimeout</span></span>|<span data-ttu-id="0c3ca-116">Valeur TimeSpan qui spécifie la durée maximale pendant laquelle l'objet peut rester inactif dans le cache avant d'être supprimé.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-116">A TimeSpan value that specifies the maximum interval of time for which the object can remain idle in the cache before being disposed.</span></span>|  
|<span data-ttu-id="0c3ca-117">leaseTimeout</span><span class="sxs-lookup"><span data-stu-id="0c3ca-117">leaseTimeout</span></span>|<span data-ttu-id="0c3ca-118">Une valeur TimeSpan qui spécifie l’intervalle de temps après lequel un objet est supprimé du cache.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-118">A TimeSpan value that specifies  the interval of time after which an object is removed from the cache.</span></span>|  
|<span data-ttu-id="0c3ca-119">maxItemsInCache</span><span class="sxs-lookup"><span data-stu-id="0c3ca-119">maxItemsInCache</span></span>|<span data-ttu-id="0c3ca-120">Entier qui spécifie le nombre maximal d'objets pouvant être placés dans le cache.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-120">An integer that specifies the maximum number of objects that can be in the cache.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0c3ca-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c3ca-121">Child Elements</span></span>  
 <span data-ttu-id="0c3ca-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0c3ca-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0c3ca-123">Parent Elements</span></span>  
  
|<span data-ttu-id="0c3ca-124">Élément</span><span class="sxs-lookup"><span data-stu-id="0c3ca-124">Element</span></span>|<span data-ttu-id="0c3ca-125">Description</span><span class="sxs-lookup"><span data-stu-id="0c3ca-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0c3ca-126">\<sendMessageChannelCache></span><span class="sxs-lookup"><span data-stu-id="0c3ca-126">\<sendMessageChannelCache></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/sendmessagechannelcache.md)|<span data-ttu-id="0c3ca-127">Comportement de service qui permet de personnaliser le partage du cache niveaux, les paramètres de cache de fabrication de canal et les paramètres du cache de canal pour les workflows qui envoient des messages aux points de terminaison de service à l’aide des activités de messagerie Send.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-127">A service behavior that enables the customization of the cache sharing levels, the settings of the channel factory cache, and the settings of the channel cache for workflows that send messages to service endpoints using Send messaging activities.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c3ca-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0c3ca-128">Remarks</span></span>  
 <span data-ttu-id="0c3ca-129">Ce comportement de service est destiné aux flux de travail qui envoient des messages aux points de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-129">This service behavior is intended for workflows that send messages to service endpoints.</span></span> <span data-ttu-id="0c3ca-130">Ces flux de travail sont généralement des flux de travail clients, mais peuvent également être des services de flux de travail hébergés dans un <xref:System.ServiceModel.WorkflowServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-130">These workflows are typically client workflows but could also be workflow services that are hosted in a <xref:System.ServiceModel.WorkflowServiceHost>.</span></span>  
  
 <span data-ttu-id="0c3ca-131">Par défaut, dans un flux de travail hébergé par un <xref:System.ServiceModel.WorkflowServiceHost>, le cache utilisé par les activités de messagerie <xref:System.ServiceModel.Activities.Send> est partagé entre toutes les instances de flux de travail dans <xref:System.ServiceModel.WorkflowServiceHost> (mise en cache au niveau de l'hôte).</span><span class="sxs-lookup"><span data-stu-id="0c3ca-131">By default, in a workflow hosted by a <xref:System.ServiceModel.WorkflowServiceHost>, the cache used by <xref:System.ServiceModel.Activities.Send> messaging activities is shared across all workflow instances in the <xref:System.ServiceModel.WorkflowServiceHost> (host-level caching).</span></span> <span data-ttu-id="0c3ca-132">Pour un flux de travail client non hébergé par un objet  <xref:System.ServiceModel.WorkflowServiceHost>, le cache est uniquement disponible pour l'instance de flux de travail (mise en cache au niveau de l'instance).</span><span class="sxs-lookup"><span data-stu-id="0c3ca-132">For a client workflow that is not hosted by a <xref:System.ServiceModel.WorkflowServiceHost>, the cache is available only to the workflow instance (instance-level caching).</span></span> <span data-ttu-id="0c3ca-133">La mise en cache est désactivée par défaut pour toute activité d'envoi dans votre flux de travail qui a des points de terminaison définis dans la configuration.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-133">Caching is disabled by default for any send activity in your workflow that has endpoints defined in configuration.</span></span>  
  
 <span data-ttu-id="0c3ca-134">Pour plus d’informations sur la modification des paramètres de cache pour la fabrication de canal et le cache de canaux et niveaux de partage de cache par défaut, consultez [changement des niveaux de partage de Cache pour les activités d’envoi](../../../../../docs/framework/wcf/feature-details/changing-the-cache-sharing-levels-for-send-activities.md).</span><span class="sxs-lookup"><span data-stu-id="0c3ca-134">For more information about how to change the default cache sharing levels and cache settings for the channel factory and channel cache, see [Changing the Cache Sharing Levels for Send Activities](../../../../../docs/framework/wcf/feature-details/changing-the-cache-sharing-levels-for-send-activities.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c3ca-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="0c3ca-135">Example</span></span>  
 <span data-ttu-id="0c3ca-136">Dans un service de flux de travail hébergé, vous pouvez spécifier les paramètres du cache de la fabrique et du cache de canaux dans le fichier de configuration de l'application.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-136">In a hosted workflow service, you can specify the factory cache and channel cache settings in the application configuration file.</span></span> <span data-ttu-id="0c3ca-137">Pour cela, ajoutez un comportement de service qui contient les paramètres des caches de la fabrique et de canaux et ajoutez-le à votre service.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-137">To do so, add a service behavior that contains the cache settings for the factory and channel cache and add this service behavior to your service.</span></span> <span data-ttu-id="0c3ca-138">L’exemple suivant montre le contenu d’un fichier de configuration qui contient le **MyChannelCacheBehavior** comportement de service avec les paramètres du cache du cache et le canal de fabrique personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-138">The following example shows the contents of a configuration file that contains the **MyChannelCacheBehavior**  service behavior with the custom factory cache and channel cache settings.</span></span> <span data-ttu-id="0c3ca-139">Ce comportement de service est ajouté au service via le **behaviorConfiguarion** attribut.</span><span class="sxs-lookup"><span data-stu-id="0c3ca-139">This service behavior is added to the service through the **behaviorConfiguarion** attribute.</span></span>  
  
```xml  
<configuration>    
  <system.serviceModel>  
    <!-- List of other config sections here -->   
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="MyChannelCacheBehavior">  
          <sendMessageChannelCache allowUnsafeCaching ="false" >  
            <!-- Control only the host level settings -->   
            <factorySettings maxItemsInCache = "8" idleTimeout = "00:05:00" leaseTimeout="10:00:00" />  
            <channelSettings maxItemsInCache = "32" idleTimeout = "00:05:00" leaseTimeout="00:06:00" />  
          </sendMessageChannelCache>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service name="MyService" behaviorConfiguration="MyChannelCacheBehavior" />  
    </services>  
  </system.serviceModel>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0c3ca-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c3ca-140">See also</span></span>

- <xref:System.ServiceModel.Activities.SendMessageChannelCache>
- <xref:System.ServiceModel.Activities.Configuration.SendMessageChannelCacheElement>
- <xref:System.ServiceModel.Activities.Send>
- <xref:System.ServiceModel.Activities.ChannelCacheSettings>
- [<span data-ttu-id="0c3ca-141">Modification des niveaux de partage du cache pour les activités d’envoi</span><span class="sxs-lookup"><span data-stu-id="0c3ca-141">Changing the Cache Sharing Levels for Send Activities</span></span>](../../../../../docs/framework/wcf/feature-details/changing-the-cache-sharing-levels-for-send-activities.md)
