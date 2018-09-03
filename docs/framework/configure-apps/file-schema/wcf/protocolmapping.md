---
title: '&lt;protocolMapping&gt;'
ms.date: 03/30/2017
ms.assetid: 5076644b-1f33-4f26-9488-87de9fcda04c
ms.openlocfilehash: 4afdaaa62c1ac3241eb7382d0995bed51bde73e2
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32748904"
---
# <a name="ltprotocolmappinggt"></a><span data-ttu-id="405d3-102">&lt;protocolMapping&gt;</span><span class="sxs-lookup"><span data-stu-id="405d3-102">&lt;protocolMapping&gt;</span></span>
<span data-ttu-id="405d3-103">Représente une section de configuration pour définir un ensemble de mappage de protocole par défaut entre les schémas de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et des liaisons WCF.</span><span class="sxs-lookup"><span data-stu-id="405d3-103">Represents a configuration section for defining a set of default protocol mapping between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and WCF bindings.</span></span> <span data-ttu-id="405d3-104">Lors de la création de points de terminaison par défaut lors de l’exécution, Windows Communication Foundation (WCF) examine les mappages configurés et décide de liaison à utiliser en une adresse de base.</span><span class="sxs-lookup"><span data-stu-id="405d3-104">When creating default endpoints at runtime, Windows Communication Foundation (WCF) looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
 <span data-ttu-id="405d3-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="405d3-105">\<system.serviceModel></span></span>  
<span data-ttu-id="405d3-106">\<protocolMapping ></span><span class="sxs-lookup"><span data-stu-id="405d3-106">\<protocolMapping></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="405d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="405d3-107">Syntax</span></span>  
  
```xml
   <protocolMapping>    <add binding="String"         bindingConfiguration="String"         scheme="http/net.msmq/net.pipe/net.tcp"/></protocolMapping>  
```

## <a name="attributes-and-elements"></a><span data-ttu-id="405d3-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="405d3-108">Attributes and Elements</span></span>  
 <span data-ttu-id="405d3-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="405d3-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="405d3-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="405d3-110">Attributes</span></span>  
 <span data-ttu-id="405d3-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="405d3-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="405d3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="405d3-112">Child Elements</span></span>  
  
|<span data-ttu-id="405d3-113">Élément</span><span class="sxs-lookup"><span data-stu-id="405d3-113">Element</span></span>|<span data-ttu-id="405d3-114">Description</span><span class="sxs-lookup"><span data-stu-id="405d3-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="405d3-115">\<filtres></span><span class="sxs-lookup"><span data-stu-id="405d3-115">\<filters></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|<span data-ttu-id="405d3-116">Contient un mappage de protocole par défaut entre un schéma de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et une liaison WCF.</span><span class="sxs-lookup"><span data-stu-id="405d3-116">Contains a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a WCF binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="405d3-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="405d3-117">Parent Elements</span></span>  
  
|<span data-ttu-id="405d3-118">Élément</span><span class="sxs-lookup"><span data-stu-id="405d3-118">Element</span></span>|<span data-ttu-id="405d3-119">Description</span><span class="sxs-lookup"><span data-stu-id="405d3-119">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="405d3-120">system.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="405d3-120">system.ServiceModel</span></span>|<span data-ttu-id="405d3-121">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="405d3-121">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="405d3-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="405d3-122">Example</span></span>  
 <span data-ttu-id="405d3-123">L'exemple de configuration suivant montre le mappage de protocole par défaut dans le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="405d3-123">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="405d3-124">Vous pouvez remplacer ce mappage par défaut au niveau de l'ordinateur en modifiant le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="405d3-124">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="405d3-125">Ou, si vous souhaitez uniquement le remplacer dans la portée d'une application, vous pouvez remplacer cette section dans le fichier de configuration de votre application et modifier le mappage pour les schémas de protocole individuels.</span><span class="sxs-lookup"><span data-stu-id="405d3-125">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
```xml  
<protocolMapping>  
        <add scheme="http" binding="basicHttpBinding"/>  
        <add scheme="net.tcp" binding="netTcpBinding"/>  
        <add scheme="net.pipe" binding="netNamedPipeBinding"/>  
        <add scheme="net.msmq" binding="netMsmqBinding"/>  
</protocolMapping>  
```  
  
## <a name="see-also"></a><span data-ttu-id="405d3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="405d3-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>    
