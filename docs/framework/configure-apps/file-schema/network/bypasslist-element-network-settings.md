---
title: '&lt;BypassList&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#bypasslist
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist
helpviewer_keywords:
- bypasslist element
- <bypasslist> element
ms.assetid: 124446b7-abb1-4e5e-a492-b64398f268f1
ms.openlocfilehash: 82a9a3e6362538fc62b4afdb010ca784590b9db9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54746336"
---
# <a name="ltbypasslistgt-element-network-settings"></a><span data-ttu-id="90fdd-102">&lt;BypassList&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="90fdd-102">&lt;bypasslist&gt; Element (Network Settings)</span></span>
<span data-ttu-id="90fdd-103">Fournit un ensemble d’expressions régulières décrivant les adresses qui n’utilisent pas un proxy.</span><span class="sxs-lookup"><span data-stu-id="90fdd-103">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>  
  
 <span data-ttu-id="90fdd-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="90fdd-104">\<configuration></span></span>  
<span data-ttu-id="90fdd-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="90fdd-105">\<system.net></span></span>  
<span data-ttu-id="90fdd-106">\<defaultProxy></span><span class="sxs-lookup"><span data-stu-id="90fdd-106">\<defaultProxy></span></span>  
<span data-ttu-id="90fdd-107">\<bypasslist></span><span class="sxs-lookup"><span data-stu-id="90fdd-107">\<bypasslist></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="90fdd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90fdd-108">Syntax</span></span>  
  
```xml  
<bypasslist>   
</bypasslist>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="90fdd-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="90fdd-109">Attributes and Elements</span></span>  
 <span data-ttu-id="90fdd-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="90fdd-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="90fdd-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="90fdd-111">Attributes</span></span>  
 <span data-ttu-id="90fdd-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="90fdd-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="90fdd-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="90fdd-113">Child Elements</span></span>  
  
|<span data-ttu-id="90fdd-114">**Élément**</span><span class="sxs-lookup"><span data-stu-id="90fdd-114">**Element**</span></span>|<span data-ttu-id="90fdd-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="90fdd-115">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="90fdd-116">add</span><span class="sxs-lookup"><span data-stu-id="90fdd-116">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-bypasslist-network-settings.md)|<span data-ttu-id="90fdd-117">Ajoute une adresse IP ou le nom DNS à la liste de contournement proxy.</span><span class="sxs-lookup"><span data-stu-id="90fdd-117">Adds an IP address or DNS name to the proxy bypass list.</span></span>|  
|[<span data-ttu-id="90fdd-118">clear</span><span class="sxs-lookup"><span data-stu-id="90fdd-118">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-bypasslist-network-settings.md)|<span data-ttu-id="90fdd-119">Efface la liste de contournement.</span><span class="sxs-lookup"><span data-stu-id="90fdd-119">Clears the bypass list.</span></span>|  
|[<span data-ttu-id="90fdd-120">remove</span><span class="sxs-lookup"><span data-stu-id="90fdd-120">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-bypasslist-network-settings.md)|<span data-ttu-id="90fdd-121">Supprime une adresse IP ou le nom DNS de la liste de contournement proxy.</span><span class="sxs-lookup"><span data-stu-id="90fdd-121">Removes an IP address or DNS name from the proxy bypass list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="90fdd-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="90fdd-122">Parent Elements</span></span>  
  
|<span data-ttu-id="90fdd-123">**Élément**</span><span class="sxs-lookup"><span data-stu-id="90fdd-123">**Element**</span></span>|<span data-ttu-id="90fdd-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="90fdd-124">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="90fdd-125">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="90fdd-125">defaultProxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|<span data-ttu-id="90fdd-126">Configure le serveur proxy HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="90fdd-126">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="90fdd-127">Notes</span><span class="sxs-lookup"><span data-stu-id="90fdd-127">Remarks</span></span>  
 <span data-ttu-id="90fdd-128">La liste de contournement contient des expressions régulières qui décrivent les URI qui <xref:System.Net.WebRequest> instances accéder directement au lieu de via le serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="90fdd-128">The bypass list contains regular expressions that describe URIs that <xref:System.Net.WebRequest> instances access directly instead of through the proxy server.</span></span>  
  
 <span data-ttu-id="90fdd-129">Soyez prudent lorsque vous spécifiez une expression régulière pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="90fdd-129">You should use caution when specifying a regular expression for this element.</span></span> <span data-ttu-id="90fdd-130">L’expression régulière « [a-z] +\\.contoso\\.com » correspond à tout hôte dans le domaine contoso.com, mais il correspond également à n’importe quel hôte dans le domaine contoso.com.cpandl.com.</span><span class="sxs-lookup"><span data-stu-id="90fdd-130">The regular expression "[a-z]+\\.contoso\\.com" matches any host in the contoso.com domain, but it also matches any host in the contoso.com.cpandl.com domain.</span></span> <span data-ttu-id="90fdd-131">Pour faire correspondre uniquement sur un ordinateur hôte dans le domaine contoso.com, utilisez une ancre (« $») : « [a-z] +\\.contoso\\.com$ ».</span><span class="sxs-lookup"><span data-stu-id="90fdd-131">To match only a host in the contoso.com domain, use an anchor ("$"): "[a-z]+\\.contoso\\.com$".</span></span>  
  
 <span data-ttu-id="90fdd-132">Pour plus d’informations sur les expressions régulières, consultez. [Expressions régulières .NET framework](../../../../../docs/standard/base-types/regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="90fdd-132">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../../docs/standard/base-types/regular-expressions.md).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="90fdd-133">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="90fdd-133">Configuration Files</span></span>  
 <span data-ttu-id="90fdd-134">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="90fdd-134">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="90fdd-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="90fdd-135">Example</span></span>  
 <span data-ttu-id="90fdd-136">L’exemple suivant ajoute deux adresses à la liste de contournement.</span><span class="sxs-lookup"><span data-stu-id="90fdd-136">The following example adds two addresses to the bypass list.</span></span> <span data-ttu-id="90fdd-137">La première contourne le proxy pour tous les serveurs dans le domaine contoso.com ; la deuxième contourne le proxy pour tous les serveurs dont les adresses IP commencent par 192.168.</span><span class="sxs-lookup"><span data-stu-id="90fdd-137">The first bypasses the proxy for all servers in the contoso.com domain; the second bypasses the proxy for all servers whose IP addresses begin with 192.168.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
        <add address="[a-z]+\.contoso\.com$" />  
        <add address="192\.168\.\d{1,3}\.\d{1,3}" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="90fdd-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90fdd-138">See also</span></span>
- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="90fdd-139">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="90fdd-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
