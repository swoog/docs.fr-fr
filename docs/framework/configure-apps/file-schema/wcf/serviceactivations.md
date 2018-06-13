---
title: '&lt;serviceActivations&gt;'
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: c62f2bd1a34aca31ea9f9d5de17840f2967b269c
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32748527"
---
# <a name="ltserviceactivationsgt"></a><span data-ttu-id="7eefc-102">&lt;serviceActivations&gt;</span><span class="sxs-lookup"><span data-stu-id="7eefc-102">&lt;serviceActivations&gt;</span></span>
<span data-ttu-id="7eefc-103">Un élément de configuration qui vous permet d’ajouter des paramètres qui définissent les paramètres d’activation de service virtuel qui correspondent à vos types de service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="7eefc-103">A configuration element that allows you to add settings that define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="7eefc-104">Cela permet d'activer des services hébergés dans WAS/IIS sans utiliser de fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="7eefc-104">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>  
  
 <span data-ttu-id="7eefc-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7eefc-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="7eefc-106">\<serviceHostingEnvironment ></span><span class="sxs-lookup"><span data-stu-id="7eefc-106">\<serviceHostingEnvironment></span></span>  
<span data-ttu-id="7eefc-107">\<serviceActivations ></span><span class="sxs-lookup"><span data-stu-id="7eefc-107">\<serviceActivations></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7eefc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7eefc-108">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>   
   <serviceActivations>  
      <add factory="String"  
           service="String"/>  
   </serviceActivations>  
</serviceHostingEnvironment>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7eefc-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7eefc-109">Attributes and Elements</span></span>  
 <span data-ttu-id="7eefc-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7eefc-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7eefc-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="7eefc-111">Attributes</span></span>  
 <span data-ttu-id="7eefc-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7eefc-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="7eefc-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7eefc-113">Child Elements</span></span>  
  
|<span data-ttu-id="7eefc-114">Élément</span><span class="sxs-lookup"><span data-stu-id="7eefc-114">Element</span></span>|<span data-ttu-id="7eefc-115">Description</span><span class="sxs-lookup"><span data-stu-id="7eefc-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7eefc-116">\<add></span><span class="sxs-lookup"><span data-stu-id="7eefc-116">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-serviceactivations.md)|<span data-ttu-id="7eefc-117">Ajoute un élément de configuration qui spécifie l'activation d'une application de service.</span><span class="sxs-lookup"><span data-stu-id="7eefc-117">Adds a configuration element that specifies the activation of a service application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7eefc-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7eefc-118">Parent Elements</span></span>  
  
|<span data-ttu-id="7eefc-119">Élément</span><span class="sxs-lookup"><span data-stu-id="7eefc-119">Element</span></span>|<span data-ttu-id="7eefc-120">Description</span><span class="sxs-lookup"><span data-stu-id="7eefc-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7eefc-121">\<serviceHostingEnvironment ></span><span class="sxs-lookup"><span data-stu-id="7eefc-121">\<serviceHostingEnvironment></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|<span data-ttu-id="7eefc-122">Définit le type instancié par l'environnement d'hébergement du service pour un transport particulier.</span><span class="sxs-lookup"><span data-stu-id="7eefc-122">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7eefc-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7eefc-123">Remarks</span></span>  
 <span data-ttu-id="7eefc-124">L'exemple suivant indique comment configurer des paramètres d'activation dans le fichier web.config.</span><span class="sxs-lookup"><span data-stu-id="7eefc-124">The following example shows how to configure activation settings within your web.config file.</span></span>  
  
```xml  
<configuration>  
  <system.serviceModel>  
    <serviceHostingEnvironment>  
      <serviceActivations>  
        <add service="GreetingService"/>  
      </serviceActivations>  
    </serviceHostingEnvironment>  
  </system.serviceModel>  
</configuration>  
```  
  
 <span data-ttu-id="7eefc-125">Cette configuration vous permet d'activer GreetingService sans utiliser de fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="7eefc-125">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>  
  
 <span data-ttu-id="7eefc-126">Notez que `<serviceHostingEnvironment>` est une configuration au niveau de l'application.</span><span class="sxs-lookup"><span data-stu-id="7eefc-126">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="7eefc-127">Vous devez placer le `web.config` qui contient la configuration sous la racine de l'application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7eefc-127">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="7eefc-128">De plus, `serviceHostingEnvironment` est une section machinetoApplication qui peut être héritée.</span><span class="sxs-lookup"><span data-stu-id="7eefc-128">In addition, `serviceHostingEnvironment` is a machinetoApplication inheritable section.</span></span> <span data-ttu-id="7eefc-129">Si vous inscrivez un seul service à la racine de l'ordinateur, chaque service dans l'application hérite de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="7eefc-129">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>  
  
 <span data-ttu-id="7eefc-130">L'activation basée sur la configuration prend en charge l'activation via un protocole HTTP ou non-HTTP.</span><span class="sxs-lookup"><span data-stu-id="7eefc-130">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="7eefc-131">Elle requiert des extensions dans relativeAddress, par exemple .svc, .xoml ou .xamlx.</span><span class="sxs-lookup"><span data-stu-id="7eefc-131">It requires extensions in the relatativeAddress i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="7eefc-132">Vous pouvez mapper vos propres extensions au buildProviders connu, qui vous permet ensuite d’activer le service sur n’importe quelle extension.</span><span class="sxs-lookup"><span data-stu-id="7eefc-132">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="7eefc-133">En cas de conflit, la section `<serviceActivations>` remplace les inscriptions .svc.</span><span class="sxs-lookup"><span data-stu-id="7eefc-133">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7eefc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7eefc-134">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>  
 <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>  
 <xref:System.ServiceModel.ServiceHostingEnvironment>
