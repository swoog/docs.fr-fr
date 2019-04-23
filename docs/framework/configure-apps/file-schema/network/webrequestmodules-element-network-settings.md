---
title: <webRequestModules>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules
- http://schemas.microsoft.com/.NetConfiguration/v2.0#webRequestModules
helpviewer_keywords:
- webRequestModules element
- <webRequestModules> element
ms.assetid: 1263de11-3e0a-4f94-97c9-710b2ae53817
ms.openlocfilehash: e5d1780a204b2e99593d51179a479845fd49e608
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59187003"
---
# <a name="webrequestmodules-element-network-settings"></a><span data-ttu-id="339d6-102">\<webRequestModules >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="339d6-102">\<webRequestModules> Element (Network Settings)</span></span>
<span data-ttu-id="339d6-103">Spécifie les modules à utiliser pour demander des informations à partir d’hôtes de réseau.</span><span class="sxs-lookup"><span data-stu-id="339d6-103">Specifies modules to use to request information from network hosts.</span></span>  
  
 <span data-ttu-id="339d6-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="339d6-104">\<configuration></span></span>  
<span data-ttu-id="339d6-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="339d6-105">\<system.net></span></span>  
<span data-ttu-id="339d6-106">\<webRequestModules></span><span class="sxs-lookup"><span data-stu-id="339d6-106">\<webRequestModules></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="339d6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="339d6-107">Syntax</span></span>  
  
```xml  
<webRequestModules>   
</webRequestModules>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="339d6-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="339d6-108">Attributes and Elements</span></span>  
 <span data-ttu-id="339d6-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="339d6-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="339d6-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="339d6-110">Attributes</span></span>  
 <span data-ttu-id="339d6-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="339d6-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="339d6-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="339d6-112">Child Elements</span></span>  
  
|<span data-ttu-id="339d6-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="339d6-113">**Element**</span></span>|<span data-ttu-id="339d6-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="339d6-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="339d6-115">add</span><span class="sxs-lookup"><span data-stu-id="339d6-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-webrequestmodules-network-settings.md)|<span data-ttu-id="339d6-116">Ajoute un module de demande Web personnalisé à l’application.</span><span class="sxs-lookup"><span data-stu-id="339d6-116">Adds a custom Web request module to the application.</span></span>|  
|[<span data-ttu-id="339d6-117">clear</span><span class="sxs-lookup"><span data-stu-id="339d6-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-webrequestmodules-network-settings.md)|<span data-ttu-id="339d6-118">Supprime tous les modules de demande Web inscrits de l’application.</span><span class="sxs-lookup"><span data-stu-id="339d6-118">Removes all registered Web request modules from the application.</span></span>|  
|[<span data-ttu-id="339d6-119">remove</span><span class="sxs-lookup"><span data-stu-id="339d6-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-webrequestmodules-network-settings.md)|<span data-ttu-id="339d6-120">Supprime un module de demande Web personnalisé de l’application.</span><span class="sxs-lookup"><span data-stu-id="339d6-120">Removes a custom Web request module from the application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="339d6-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="339d6-121">Parent Elements</span></span>  
  
|<span data-ttu-id="339d6-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="339d6-122">**Element**</span></span>|<span data-ttu-id="339d6-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="339d6-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="339d6-124">system.net</span><span class="sxs-lookup"><span data-stu-id="339d6-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="339d6-125">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="339d6-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="339d6-126">Notes</span><span class="sxs-lookup"><span data-stu-id="339d6-126">Remarks</span></span>  
 <span data-ttu-id="339d6-127">Le `webRequestModules` élément inscrit les descendants de le <xref:System.Net.WebRequest> classe pour gérer les demandes d’informations sur les hôtes de réseau.</span><span class="sxs-lookup"><span data-stu-id="339d6-127">The `webRequestModules` element registers descendants of the <xref:System.Net.WebRequest> class to handle information requests to network hosts.</span></span> <span data-ttu-id="339d6-128">Modules de demande Web doivent implémenter le <xref:System.Net.IWebRequestCreate> interface.</span><span class="sxs-lookup"><span data-stu-id="339d6-128">Web request modules must implement the <xref:System.Net.IWebRequestCreate> interface.</span></span>  
  
 <span data-ttu-id="339d6-129">Le .NET Framework inclut des modules de demande Web pour les URI qui commencent par `http://`, `https://`, et `file://`.</span><span class="sxs-lookup"><span data-stu-id="339d6-129">The .NET Framework includes Web request modules for URIs that begin with `http://`, `https://`, and `file://`.</span></span> <span data-ttu-id="339d6-130">Vous pouvez remplacer les modules par défaut qu’en inscrivant un module personnalisé dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="339d6-130">You can override the default modules only by registering a custom module in the configuration file.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="339d6-131">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="339d6-131">Configuration Files</span></span>  
 <span data-ttu-id="339d6-132">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="339d6-132">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="339d6-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="339d6-133">Example</span></span>  
 <span data-ttu-id="339d6-134">L’exemple suivant inscrit le module HTTP par défaut.</span><span class="sxs-lookup"><span data-stu-id="339d6-134">The following example registers the default HTTP module.</span></span> <span data-ttu-id="339d6-135">Vous devez remplacer les valeurs de Version et PublicKeyToken par les valeurs correctes pour le module spécifié.</span><span class="sxs-lookup"><span data-stu-id="339d6-135">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="339d6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="339d6-136">See also</span></span>

- <xref:System.Net.WebRequest>
- <xref:System.Net.IWebRequestCreate>
- [<span data-ttu-id="339d6-137">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="339d6-137">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
