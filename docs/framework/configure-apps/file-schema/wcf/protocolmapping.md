---
title: <protocolMapping>
ms.date: 03/30/2017
ms.assetid: 5076644b-1f33-4f26-9488-87de9fcda04c
ms.openlocfilehash: e26044340bda84fe38b7e286edf833affa94b86c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785487"
---
# <a name="protocolmapping"></a><span data-ttu-id="b13c8-101">\<protocolMapping></span><span class="sxs-lookup"><span data-stu-id="b13c8-101">\<protocolMapping></span></span>
<span data-ttu-id="b13c8-102">Représente une section de configuration pour définir un ensemble de mappage de protocole par défaut entre les schémas de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et des liaisons WCF.</span><span class="sxs-lookup"><span data-stu-id="b13c8-102">Represents a configuration section for defining a set of default protocol mapping between transport protocol schemes (e.g., http, net.tcp, net.pipe, etc.) and WCF bindings.</span></span> <span data-ttu-id="b13c8-103">Lorsque vous créez des points de terminaison par défaut lors de l’exécution, Windows Communication Foundation (WCF) examine les mappages configurés et décide de liaison à utiliser en tant qu’adresse de base.</span><span class="sxs-lookup"><span data-stu-id="b13c8-103">When creating default endpoints at runtime, Windows Communication Foundation (WCF) looks at the configured mappings and decides on which binding to use for a particular based address.</span></span>  
  
[<span data-ttu-id="b13c8-104">**\<system.serviceModel>**</span><span class="sxs-lookup"><span data-stu-id="b13c8-104">**\<system.serviceModel>**</span></span>](system-servicemodel.md)  
<span data-ttu-id="b13c8-105">&nbsp;&nbsp;**\<protocolMapping>**</span><span class="sxs-lookup"><span data-stu-id="b13c8-105">&nbsp;&nbsp;**\<protocolMapping>**</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b13c8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b13c8-106">Syntax</span></span>  
  
```xml  
<protocolMapping>
  <add binding="String"
       bindingConfiguration="String"
       scheme="http/net.msmq/net.pipe/net.tcp" />
</protocolMapping>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b13c8-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b13c8-107">Attributes and Elements</span></span>  
 <span data-ttu-id="b13c8-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b13c8-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b13c8-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="b13c8-109">Attributes</span></span>  
 <span data-ttu-id="b13c8-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b13c8-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b13c8-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b13c8-111">Child Elements</span></span>  
  
|<span data-ttu-id="b13c8-112">Élément</span><span class="sxs-lookup"><span data-stu-id="b13c8-112">Element</span></span>|<span data-ttu-id="b13c8-113">Description</span><span class="sxs-lookup"><span data-stu-id="b13c8-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b13c8-114">\<filtres></span><span class="sxs-lookup"><span data-stu-id="b13c8-114">\<filters></span></span>](filters-of-routing.md)|<span data-ttu-id="b13c8-115">Contient un mappage de protocole par défaut entre un schéma de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et une liaison WCF.</span><span class="sxs-lookup"><span data-stu-id="b13c8-115">Contains a default protocol mapping between a transport protocol scheme (e.g., http, net.tcp, net.pipe, etc.) and a WCF binding.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b13c8-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b13c8-116">Parent Elements</span></span>  
  
|<span data-ttu-id="b13c8-117">Élément</span><span class="sxs-lookup"><span data-stu-id="b13c8-117">Element</span></span>|<span data-ttu-id="b13c8-118">Description</span><span class="sxs-lookup"><span data-stu-id="b13c8-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b13c8-119">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="b13c8-119">\<system.serviceModel></span></span>](system-servicemodel.md)|<span data-ttu-id="b13c8-120">Élément racine de tous les éléments de configuration WCF.</span><span class="sxs-lookup"><span data-stu-id="b13c8-120">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b13c8-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="b13c8-121">Example</span></span>  
 <span data-ttu-id="b13c8-122">L'exemple de configuration suivant montre le mappage de protocole par défaut dans le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="b13c8-122">The following configuration example shows the default protocol mapping in the machine.config file.</span></span> <span data-ttu-id="b13c8-123">Vous pouvez remplacer ce mappage par défaut au niveau de l'ordinateur en modifiant le fichier machine.config.</span><span class="sxs-lookup"><span data-stu-id="b13c8-123">You can override this default mapping at the machine level by modifying the machine.config file.</span></span> <span data-ttu-id="b13c8-124">Ou, si vous souhaitez uniquement le remplacer dans la portée d'une application, vous pouvez remplacer cette section dans le fichier de configuration de votre application et modifier le mappage pour les schémas de protocole individuels.</span><span class="sxs-lookup"><span data-stu-id="b13c8-124">Or if you would only like to override it within the scope of an application, you can override this section within your application configuration file and change the mapping for individual protocol schemes.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="b13c8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b13c8-125">See also</span></span>

- <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>
- <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>
