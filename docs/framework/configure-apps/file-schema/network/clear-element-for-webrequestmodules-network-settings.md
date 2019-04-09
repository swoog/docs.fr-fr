---
title: <clear> Élément de webRequestModules (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- <clear> element, webRequestModules
- <webRequestModules>, clear element
- webRequestModules, clear element
- clear element, webRequestModules
ms.assetid: 48f38bcb-f30c-4b74-a8f0-1a3caf1aa96f
ms.openlocfilehash: 5dea238629b282776cb45f7b388e655fa557d084
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59078978"
---
# <a name="clear-element-for-webrequestmodules-network-settings"></a><span data-ttu-id="14730-102">\<Désactivez >, élément de webRequestModules (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="14730-102">\<clear> Element for webRequestModules (Network Settings)</span></span>
<span data-ttu-id="14730-103">Supprime tous les modules de demande Web inscrits de l’application.</span><span class="sxs-lookup"><span data-stu-id="14730-103">Removes all registered Web request modules from the application.</span></span>  
  
 <span data-ttu-id="14730-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="14730-104">\<configuration></span></span>  
<span data-ttu-id="14730-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="14730-105">\<system.net></span></span>  
<span data-ttu-id="14730-106">\<webRequestModules></span><span class="sxs-lookup"><span data-stu-id="14730-106">\<webRequestModules></span></span>  
<span data-ttu-id="14730-107">\<clear></span><span class="sxs-lookup"><span data-stu-id="14730-107">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="14730-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14730-108">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="14730-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="14730-109">Attributes and Elements</span></span>  
 <span data-ttu-id="14730-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="14730-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="14730-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="14730-111">Attributes</span></span>  
 <span data-ttu-id="14730-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="14730-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="14730-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="14730-113">Child Elements</span></span>  
 <span data-ttu-id="14730-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="14730-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="14730-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="14730-115">Parent Elements</span></span>  
  
|**<span data-ttu-id="14730-116">Élément</span><span class="sxs-lookup"><span data-stu-id="14730-116">Element</span></span>**|**<span data-ttu-id="14730-117">Description</span><span class="sxs-lookup"><span data-stu-id="14730-117">Description</span></span>**|  
|-----------------|---------------------|  
|[<span data-ttu-id="14730-118">webRequestModules</span><span class="sxs-lookup"><span data-stu-id="14730-118">webRequestModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|<span data-ttu-id="14730-119">Spécifie les modules à utiliser pour demander des informations à partir d’hôtes de réseau.</span><span class="sxs-lookup"><span data-stu-id="14730-119">Specifies modules to use to request information from network hosts.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="14730-120">Notes</span><span class="sxs-lookup"><span data-stu-id="14730-120">Remarks</span></span>  
 <span data-ttu-id="14730-121">Le `clear` élément supprime inscrits tous les modules de demande Web qui ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.</span><span class="sxs-lookup"><span data-stu-id="14730-121">The `clear` element removes all registered Web request modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="14730-122">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="14730-122">Configuration Files</span></span>  
 <span data-ttu-id="14730-123">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="14730-123">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="14730-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="14730-124">Example</span></span>  
 <span data-ttu-id="14730-125">L’exemple suivant efface tous les modules de demande Web et inscrit un module de demande Web pour HTTP.</span><span class="sxs-lookup"><span data-stu-id="14730-125">The following example clears all Web request modules and then registers a Web request module for HTTP.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <clear/>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="14730-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14730-126">See also</span></span>

- <xref:System.Net.WebRequest>
- [<span data-ttu-id="14730-127">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="14730-127">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
