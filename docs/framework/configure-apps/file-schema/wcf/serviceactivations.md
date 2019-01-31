---
title: <serviceActivations>
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: 7a091ecfbc0f4773ece620f93a9f21c219fcccb6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55256702"
---
# <a name="serviceactivations"></a><span data-ttu-id="b433c-101">\<serviceActivations></span><span class="sxs-lookup"><span data-stu-id="b433c-101">\<serviceActivations></span></span>
<span data-ttu-id="b433c-102">Un élément de configuration qui vous permet d’ajouter des paramètres qui définissent les paramètres d’activation de service virtuel qui correspondent à vos types de service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="b433c-102">A configuration element that allows you to add settings that define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="b433c-103">Cela permet d'activer des services hébergés dans WAS/IIS sans utiliser de fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="b433c-103">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>  
  
 <span data-ttu-id="b433c-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b433c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b433c-105">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="b433c-105">\<serviceHostingEnvironment></span></span>  
<span data-ttu-id="b433c-106">\<serviceActivations></span><span class="sxs-lookup"><span data-stu-id="b433c-106">\<serviceActivations></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b433c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b433c-107">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <serviceActivations>
    <add factory="String"
         service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b433c-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b433c-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b433c-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b433c-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b433c-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="b433c-110">Attributes</span></span>  
 <span data-ttu-id="b433c-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b433c-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b433c-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b433c-112">Child Elements</span></span>  
  
|<span data-ttu-id="b433c-113">Élément</span><span class="sxs-lookup"><span data-stu-id="b433c-113">Element</span></span>|<span data-ttu-id="b433c-114">Description</span><span class="sxs-lookup"><span data-stu-id="b433c-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b433c-115">\<add></span><span class="sxs-lookup"><span data-stu-id="b433c-115">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-serviceactivations.md)|<span data-ttu-id="b433c-116">Ajoute un élément de configuration qui spécifie l'activation d'une application de service.</span><span class="sxs-lookup"><span data-stu-id="b433c-116">Adds a configuration element that specifies the activation of a service application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b433c-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b433c-117">Parent Elements</span></span>  
  
|<span data-ttu-id="b433c-118">Élément</span><span class="sxs-lookup"><span data-stu-id="b433c-118">Element</span></span>|<span data-ttu-id="b433c-119">Description</span><span class="sxs-lookup"><span data-stu-id="b433c-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b433c-120">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="b433c-120">\<serviceHostingEnvironment></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|<span data-ttu-id="b433c-121">Définit le type instancié par l'environnement d'hébergement du service pour un transport particulier.</span><span class="sxs-lookup"><span data-stu-id="b433c-121">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b433c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b433c-122">Remarks</span></span>  
 <span data-ttu-id="b433c-123">L'exemple suivant indique comment configurer des paramètres d'activation dans le fichier web.config.</span><span class="sxs-lookup"><span data-stu-id="b433c-123">The following example shows how to configure activation settings within your web.config file.</span></span>  
  
```xml  
<configuration>
  <system.serviceModel>
    <serviceHostingEnvironment>
      <serviceActivations>
        <add service="GreetingService" />
      </serviceActivations>
    </serviceHostingEnvironment>
  </system.serviceModel>
</configuration>
```  
  
 <span data-ttu-id="b433c-124">Cette configuration vous permet d'activer GreetingService sans utiliser de fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="b433c-124">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>  
  
 <span data-ttu-id="b433c-125">Notez que `<serviceHostingEnvironment>` est une configuration au niveau de l'application.</span><span class="sxs-lookup"><span data-stu-id="b433c-125">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="b433c-126">Vous devez placer le `web.config` qui contient la configuration sous la racine de l'application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b433c-126">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="b433c-127">De plus, `serviceHostingEnvironment` est une section machinetoApplication qui peut être héritée.</span><span class="sxs-lookup"><span data-stu-id="b433c-127">In addition, `serviceHostingEnvironment` is a machinetoApplication inheritable section.</span></span> <span data-ttu-id="b433c-128">Si vous inscrivez un seul service à la racine de l'ordinateur, chaque service dans l'application hérite de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b433c-128">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>  
  
 <span data-ttu-id="b433c-129">L'activation basée sur la configuration prend en charge l'activation via un protocole HTTP ou non-HTTP.</span><span class="sxs-lookup"><span data-stu-id="b433c-129">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="b433c-130">Elle requiert des extensions dans relativeAddress, par exemple .svc, .xoml ou .xamlx.</span><span class="sxs-lookup"><span data-stu-id="b433c-130">It requires extensions in the relatativeAddress i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="b433c-131">Vous pouvez mapper vos propres extensions au buildProviders connu, qui vous permet ensuite d’activer le service sur n’importe quelle extension.</span><span class="sxs-lookup"><span data-stu-id="b433c-131">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="b433c-132">En cas de conflit, la section `<serviceActivations>` remplace les inscriptions .svc.</span><span class="sxs-lookup"><span data-stu-id="b433c-132">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b433c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b433c-133">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
