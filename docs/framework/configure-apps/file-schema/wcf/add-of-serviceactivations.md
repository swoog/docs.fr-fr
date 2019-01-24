---
title: '&lt;add&gt; de &lt;serviceActivations&gt;'
ms.date: 03/30/2017
ms.assetid: e5b01fc8-ee84-48b7-95fd-95ab54fa871f
ms.openlocfilehash: d0e1f45cc8ff5b544eff5ff5dae33d5989aaf405
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587633"
---
# <a name="ltaddgt-of-ltserviceactivationsgt"></a><span data-ttu-id="3ef22-102">&lt;add&gt; de &lt;serviceActivations&gt;</span><span class="sxs-lookup"><span data-stu-id="3ef22-102">&lt;add&gt; of &lt;serviceActivations&gt;</span></span>
<span data-ttu-id="3ef22-103">Un élément de configuration qui vous permet de définir les paramètres d’activation de service virtuel qui correspondent à vos types de service Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="3ef22-103">A configuration element that allows you to define virtual service activation settings that map to your Windows Communication Foundation (WCF) service types.</span></span> <span data-ttu-id="3ef22-104">Cela permet d'activer des services hébergés dans WAS/IIS sans utiliser de fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="3ef22-104">This makes it possible to activate services hosted in WAS/IIS without an .svc file.</span></span>  
  
 <span data-ttu-id="3ef22-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="3ef22-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="3ef22-106">\<ServiceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="3ef22-106">\<ServiceHostingEnvironment></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ef22-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ef22-107">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
    <serviceActivations>
      <add factory="String"
           service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3ef22-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3ef22-108">Attributes and Elements</span></span>  
 <span data-ttu-id="3ef22-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="3ef22-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3ef22-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ef22-110">Attributes</span></span>  
  
|<span data-ttu-id="3ef22-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="3ef22-111">Attribute</span></span>|<span data-ttu-id="3ef22-112">Description</span><span class="sxs-lookup"><span data-stu-id="3ef22-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3ef22-113">factory</span><span class="sxs-lookup"><span data-stu-id="3ef22-113">factory</span></span>|<span data-ttu-id="3ef22-114">Chaîne qui spécifie le nom de type CLR de la fabrique qui génère un élément d'activation de service.</span><span class="sxs-lookup"><span data-stu-id="3ef22-114">A string that specifies the CLR type name of the factory that generates a service activation element.</span></span>|  
|<span data-ttu-id="3ef22-115">service</span><span class="sxs-lookup"><span data-stu-id="3ef22-115">service</span></span>|<span data-ttu-id="3ef22-116">Le ServiceType qui implémente le service (Typename qualifié complet ou Typename court (s'il est placé dans le dossier App_Code).</span><span class="sxs-lookup"><span data-stu-id="3ef22-116">The ServiceType that implements the service (either the full qualified Typename or the short Typename (when it is placed in the App_Code folder).</span></span>|  
|<span data-ttu-id="3ef22-117">relativeAddress</span><span class="sxs-lookup"><span data-stu-id="3ef22-117">relativeAddress</span></span>|<span data-ttu-id="3ef22-118">L'adresse relative dans l'application IIS active (par exemple « Service.svc ».</span><span class="sxs-lookup"><span data-stu-id="3ef22-118">The relative address within the current IIS application - for example "Service.svc".</span></span> <span data-ttu-id="3ef22-119">Dans WCF 4.0 cette adresse relative doit contenir une des extensions de fichiers connues (.svc, .xamlx,…). Aucun fichier physique ne doit exister pour relativeUrl.</span><span class="sxs-lookup"><span data-stu-id="3ef22-119">In WCF 4.0 this relative address has to contain one of the known file extensions (.svc, .xamlx, ...). No physical file has to exist for the relativeUrl</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3ef22-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3ef22-120">Child Elements</span></span>  
 <span data-ttu-id="3ef22-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3ef22-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3ef22-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3ef22-122">Parent Elements</span></span>  
  
|<span data-ttu-id="3ef22-123">Élément</span><span class="sxs-lookup"><span data-stu-id="3ef22-123">Element</span></span>|<span data-ttu-id="3ef22-124">Description</span><span class="sxs-lookup"><span data-stu-id="3ef22-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3ef22-125">\<serviceHostingEnvironment></span><span class="sxs-lookup"><span data-stu-id="3ef22-125">\<serviceHostingEnvironment></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|<span data-ttu-id="3ef22-126">Section de configuration qui décrit les paramètres d'activation.</span><span class="sxs-lookup"><span data-stu-id="3ef22-126">A configuration section that describes activation settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3ef22-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3ef22-127">Remarks</span></span>  
 <span data-ttu-id="3ef22-128">L'exemple suivant indique comment configurer des paramètres d'activation dans le fichier web.config.</span><span class="sxs-lookup"><span data-stu-id="3ef22-128">The following example shows how to configure activation settings within your web.config file.</span></span>  
  
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
  
 <span data-ttu-id="3ef22-129">Cette configuration vous permet d'activer GreetingService sans utiliser de fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="3ef22-129">Using this configuration, you can activate the GreetingService without using an .svc file.</span></span>  
  
 <span data-ttu-id="3ef22-130">Notez que `<serviceHostingEnvironment>` est une configuration au niveau de l'application.</span><span class="sxs-lookup"><span data-stu-id="3ef22-130">Note that `<serviceHostingEnvironment>` is an application level configuration.</span></span> <span data-ttu-id="3ef22-131">Vous devez placer le `web.config` qui contient la configuration sous la racine de l'application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3ef22-131">You have to place the `web.config` containing the configuration under the root of the virtual Application.</span></span> <span data-ttu-id="3ef22-132">De plus, `serviceHostingEnvironment` est une section machinetoApplication qui peut être héritée.</span><span class="sxs-lookup"><span data-stu-id="3ef22-132">In addition, `serviceHostingEnvironment` is a machinetoApplication inheritable section.</span></span> <span data-ttu-id="3ef22-133">Si vous inscrivez un seul service à la racine de l'ordinateur, chaque service dans l'application hérite de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3ef22-133">If you register a single service in the root of the machine, every service in the application will inherit this service.</span></span>  
  
 <span data-ttu-id="3ef22-134">L'activation basée sur la configuration prend en charge l'activation via un protocole HTTP ou non-HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ef22-134">Configuration-based activation supports activation over both http and non-http protocol.</span></span> <span data-ttu-id="3ef22-135">Elle requiert des extensions dans relativeAddress, par exemple .svc, .xoml ou .xamlx.</span><span class="sxs-lookup"><span data-stu-id="3ef22-135">It requires extensions in the relatativeAddress, i.e. .svc, .xoml or .xamlx.</span></span> <span data-ttu-id="3ef22-136">Vous pouvez mapper vos propres extensions au buildProviders connu, qui vous permet ensuite d’activer le service sur n’importe quelle extension.</span><span class="sxs-lookup"><span data-stu-id="3ef22-136">You can map your own extensions to the know buildProviders, which will then enable you to activate service over any extension.</span></span> <span data-ttu-id="3ef22-137">En cas de conflit, la section `<serviceActivations>` remplace les inscriptions .svc.</span><span class="sxs-lookup"><span data-stu-id="3ef22-137">Upon conflict, the `<serviceActivations>` section overrides .svc registrations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ef22-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ef22-138">See also</span></span>
- <xref:System.ServiceModel.Configuration.ServiceActivationElement>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
