---
title: '&lt;supprimer&gt; , élément de bypasslist (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy/bypasslist/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- <bypasslist>, remove element
- remove elemment, bypasslist
- bypasslist, remove element
- remove element, bypasslist
ms.assetid: 61dcfb4a-e3d9-4abf-a2cd-7d685fe2f64b
author: mcleblanc
ms.author: markl
ms.openlocfilehash: b6c72d9780088fddcaa59e644ff8069afbb4e43d
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47074977"
---
# <a name="ltremovegt-element-for-bypasslist-network-settings"></a><span data-ttu-id="46ec9-102">&lt;supprimer&gt; , élément de bypasslist (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="46ec9-102">&lt;remove&gt; Element for bypasslist (Network Settings)</span></span>
<span data-ttu-id="46ec9-103">Supprime une adresse IP ou le nom DNS de la liste de contournement proxy.</span><span class="sxs-lookup"><span data-stu-id="46ec9-103">Removes an IP address or DNS name from the proxy bypass list.</span></span>  
  
 <span data-ttu-id="46ec9-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="46ec9-104">\<configuration></span></span>  
<span data-ttu-id="46ec9-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="46ec9-105">\<system.net></span></span>  
<span data-ttu-id="46ec9-106">\<defaultProxy ></span><span class="sxs-lookup"><span data-stu-id="46ec9-106">\<defaultProxy></span></span>  
<span data-ttu-id="46ec9-107">\<BypassList ></span><span class="sxs-lookup"><span data-stu-id="46ec9-107">\<bypasslist></span></span>  
<span data-ttu-id="46ec9-108">\<remove></span><span class="sxs-lookup"><span data-stu-id="46ec9-108">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="46ec9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46ec9-109">Syntax</span></span>  
  
```xml  
<remove   
  address="regular expression"   
/>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="46ec9-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="46ec9-110">Attributes and Elements</span></span>  
 <span data-ttu-id="46ec9-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="46ec9-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="46ec9-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="46ec9-112">Attributes</span></span>  
  
|<span data-ttu-id="46ec9-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="46ec9-113">**Attribute**</span></span>|<span data-ttu-id="46ec9-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="46ec9-114">**Description**</span></span>|  
|-------------------|---------------------|  
|`address`|<span data-ttu-id="46ec9-115">Une expression régulière décrivant une adresse IP ou un nom DNS.</span><span class="sxs-lookup"><span data-stu-id="46ec9-115">A regular expression describing an IP address or DNS name.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="46ec9-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="46ec9-116">Child Elements</span></span>  
 <span data-ttu-id="46ec9-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="46ec9-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="46ec9-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="46ec9-118">Parent Elements</span></span>  
  
|<span data-ttu-id="46ec9-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="46ec9-119">**Element**</span></span>|<span data-ttu-id="46ec9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="46ec9-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="46ec9-121">BypassList</span><span class="sxs-lookup"><span data-stu-id="46ec9-121">bypasslist</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|<span data-ttu-id="46ec9-122">Fournit un ensemble d’expressions régulières décrivant les adresses qui n’utilisent pas un proxy.</span><span class="sxs-lookup"><span data-stu-id="46ec9-122">Provides a set of regular expressions that describe addresses that do not use a proxy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46ec9-123">Notes</span><span class="sxs-lookup"><span data-stu-id="46ec9-123">Remarks</span></span>  
 <span data-ttu-id="46ec9-124">Le `remove` élément supprime des expressions régulières décrivant les adresses IP ou des noms de serveur DNS dans la liste des adresses qui contournent un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="46ec9-124">The `remove` element removes regular expressions describing IP addresses or DNS server names from the list of addresses that bypass a proxy server.</span></span> <span data-ttu-id="46ec9-125">Les adresses ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.</span><span class="sxs-lookup"><span data-stu-id="46ec9-125">The addresses were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
 <span data-ttu-id="46ec9-126">La valeur de la `address` attribut doit être une expression régulière qui décrit un ensemble d’adresses IP ou noms d’hôte.</span><span class="sxs-lookup"><span data-stu-id="46ec9-126">The value for the `address` attribute should be a regular expression that describes a set of IP addresses or host names.</span></span>  
  
 <span data-ttu-id="46ec9-127">Pour plus d’informations sur les expressions régulières, consultez. [Expressions régulières .NET framework](../../../../../docs/standard/base-types/regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="46ec9-127">For more information about regular expressions, see .[.NET Framework Regular Expressions](../../../../../docs/standard/base-types/regular-expressions.md).</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="46ec9-128">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="46ec9-128">Configuration Files</span></span>  
 <span data-ttu-id="46ec9-129">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="46ec9-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="46ec9-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="46ec9-130">Example</span></span>  
 <span data-ttu-id="46ec9-131">L’exemple suivant supprime toute définition précédente pour le domaine adventure-works.com, puis ajoute le domaine contoso.com à la liste de contournement.</span><span class="sxs-lookup"><span data-stu-id="46ec9-131">The following example removes any previous definition for the adventure-works.com domain, and then adds the contoso.com domain to the bypass list.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <bypasslist>  
        <remove address="[a-z]+\.adventure-works\.com$" />  
        <add address="[a-z]+\.contoso\.com$" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="46ec9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ec9-132">See Also</span></span>  
 <xref:System.Net.WebProxy?displayProperty=nameWithType>  
 [<span data-ttu-id="46ec9-133">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="46ec9-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
