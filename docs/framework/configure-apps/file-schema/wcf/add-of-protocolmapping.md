---
title: <add> de <protocolMapping>
ms.date: 03/30/2017
ms.assetid: 08e62249-1641-41d1-91b1-66d7b46244e4
ms.openlocfilehash: 85d09c920de2ca1ab4971551ff98ea58c4492f44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61704490"
---
# <a name="add-of-protocolmapping"></a><span data-ttu-id="b2b6a-102">\<add> of \<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="b2b6a-102">\<add> of \<protocolMapping></span></span>
<span data-ttu-id="b2b6a-103">Représente un mappage de protocole par défaut entre un schéma de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et une liaison Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="b2b6a-103">Represents a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a Windows Communication Foundation (WCF) binding.</span></span> <span data-ttu-id="b2b6a-104">Lorsque vous créez des points de terminaison par défaut lors de l’exécution, WCF examine les mappages configurés et décide de liaison à utiliser en tant qu’adresse de base.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-104">When creating default endpoints at runtime, WCF looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
 <span data-ttu-id="b2b6a-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b2b6a-105">\<system.serviceModel></span></span>  
<span data-ttu-id="b2b6a-106">\<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="b2b6a-106">\<protocolMapping></span></span>  
<span data-ttu-id="b2b6a-107">\<add></span><span class="sxs-lookup"><span data-stu-id="b2b6a-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2b6a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2b6a-108">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b2b6a-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b2b6a-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b2b6a-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b2b6a-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="b2b6a-111">Attributes</span></span>  
  
|<span data-ttu-id="b2b6a-112">Élément</span><span class="sxs-lookup"><span data-stu-id="b2b6a-112">Element</span></span>|<span data-ttu-id="b2b6a-113">Description</span><span class="sxs-lookup"><span data-stu-id="b2b6a-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b2b6a-114">liaison</span><span class="sxs-lookup"><span data-stu-id="b2b6a-114">binding</span></span>|<span data-ttu-id="b2b6a-115">Chaîne qui spécifie le type de liaison à utiliser pour un point de terminaison pendant la création de points de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-115">A string that specifies the type of binding to be used for an endpoint during default endpoint creation.</span></span>|  
|<span data-ttu-id="b2b6a-116">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2b6a-116">bindingConfiguration</span></span>|<span data-ttu-id="b2b6a-117">Chaîne qui spécifie le nom de la section de configuration de liaison à référencer.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-117">A string that specifies the name of the binding configuration section to be referenced.</span></span>|  
|<span data-ttu-id="b2b6a-118">scheme</span><span class="sxs-lookup"><span data-stu-id="b2b6a-118">scheme</span></span>|<span data-ttu-id="b2b6a-119">Schéma de protocole de transport à utiliser pour le point de terminaison par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-119">The transport protocol scheme to be used for the default endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b2b6a-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b2b6a-120">Child Elements</span></span>  
 <span data-ttu-id="b2b6a-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b2b6a-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b2b6a-122">Parent Elements</span></span>  
  
|<span data-ttu-id="b2b6a-123">Élément</span><span class="sxs-lookup"><span data-stu-id="b2b6a-123">Element</span></span>|<span data-ttu-id="b2b6a-124">Description</span><span class="sxs-lookup"><span data-stu-id="b2b6a-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b2b6a-125">\<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="b2b6a-125">\<protocolMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/protocolmapping.md)|<span data-ttu-id="b2b6a-126">Représente une section de configuration pour la définition des mappages de protocole par défaut entre les schémas de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et des liaisons Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="b2b6a-126">Represents a configuration section for defining default protocol mappings between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and Windows Communication Foundation (WCF) bindings.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b2b6a-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="b2b6a-127">Example</span></span>  
 <span data-ttu-id="b2b6a-128">L'exemple de configuration suivant montre le mappage de protocole par défaut dans le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-128">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="b2b6a-129">Vous pouvez remplacer ce mappage par défaut au niveau de l'ordinateur en modifiant le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-129">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="b2b6a-130">Ou, si vous souhaitez uniquement le remplacer dans la portée d'une application, vous pouvez remplacer cette section dans le fichier de configuration de votre application et modifier le mappage pour les schémas de protocole individuels.</span><span class="sxs-lookup"><span data-stu-id="b2b6a-130">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
```xml  
<protocolMapping>
  <add scheme="http"
       binding="basicHttpBinding" />
  <add scheme="net.tcp"
       binding="netTcpBinding" />
  <add scheme="net.pipe"
       binding="netNamedPipeBinding" />
  <add scheme="net.msmq"
       binding="netMsmqBinding" />
</protocolMapping>
```  
  
## <a name="see-also"></a><span data-ttu-id="b2b6a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2b6a-131">See also</span></span>

- <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>
