---
title: '&lt;protocolMapping&gt;'
ms.date: 03/30/2017
ms.assetid: 5076644b-1f33-4f26-9488-87de9fcda04c
ms.openlocfilehash: a376f1eaa7c8790cf2174335749ed3001b403967
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147302"
---
# <a name="ltprotocolmappinggt"></a><span data-ttu-id="a3ec3-102">&lt;protocolMapping&gt;</span><span class="sxs-lookup"><span data-stu-id="a3ec3-102">&lt;protocolMapping&gt;</span></span>
<span data-ttu-id="a3ec3-103">Représente une section de configuration pour définir un ensemble de mappage de protocole par défaut entre les schémas de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et des liaisons WCF.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-103">Represents a configuration section for defining a set of default protocol mapping between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and WCF bindings.</span></span> <span data-ttu-id="a3ec3-104">Lorsque vous créez des points de terminaison par défaut lors de l’exécution, Windows Communication Foundation (WCF) examine les mappages configurés et décide de liaison à utiliser en tant qu’adresse de base.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-104">When creating default endpoints at runtime, Windows Communication Foundation (WCF) looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
[<span data-ttu-id="a3ec3-105">**\<system.serviceModel >**</span><span class="sxs-lookup"><span data-stu-id="a3ec3-105">**\<system.serviceModel>**</span></span>](system-servicemodel.md)  
<span data-ttu-id="a3ec3-106">&nbsp;&nbsp;**\<protocolMapping >**</span><span class="sxs-lookup"><span data-stu-id="a3ec3-106">&nbsp;&nbsp;**\<protocolMapping>**</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3ec3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3ec3-107">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a3ec3-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a3ec3-108">Attributes and Elements</span></span>  
 <span data-ttu-id="a3ec3-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a3ec3-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="a3ec3-110">Attributes</span></span>  
 <span data-ttu-id="a3ec3-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a3ec3-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a3ec3-112">Child Elements</span></span>  
  
|<span data-ttu-id="a3ec3-113">Élément</span><span class="sxs-lookup"><span data-stu-id="a3ec3-113">Element</span></span>|<span data-ttu-id="a3ec3-114">Description</span><span class="sxs-lookup"><span data-stu-id="a3ec3-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a3ec3-115">\<filtres></span><span class="sxs-lookup"><span data-stu-id="a3ec3-115">\<filters></span></span>](filters-of-routing.md)|<span data-ttu-id="a3ec3-116">Contient un mappage de protocole par défaut entre un schéma de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et une liaison WCF.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-116">Contains a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a WCF binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a3ec3-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a3ec3-117">Parent Elements</span></span>  
  
|<span data-ttu-id="a3ec3-118">Élément</span><span class="sxs-lookup"><span data-stu-id="a3ec3-118">Element</span></span>|<span data-ttu-id="a3ec3-119">Description</span><span class="sxs-lookup"><span data-stu-id="a3ec3-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a3ec3-120">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="a3ec3-120">\<system.serviceModel></span></span>](system-servicemodel.md)|<span data-ttu-id="a3ec3-121">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-121">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a3ec3-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3ec3-122">Example</span></span>  
 <span data-ttu-id="a3ec3-123">L'exemple de configuration suivant montre le mappage de protocole par défaut dans le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-123">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="a3ec3-124">Vous pouvez remplacer ce mappage par défaut au niveau de l'ordinateur en modifiant le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-124">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="a3ec3-125">Ou, si vous souhaitez uniquement le remplacer dans la portée d'une application, vous pouvez remplacer cette section dans le fichier de configuration de votre application et modifier le mappage pour les schémas de protocole individuels.</span><span class="sxs-lookup"><span data-stu-id="a3ec3-125">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="a3ec3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3ec3-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>    
