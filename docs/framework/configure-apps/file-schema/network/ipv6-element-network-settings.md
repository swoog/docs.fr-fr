---
title: '&lt;IPv6&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/ipv6
- http://schemas.microsoft.com/.NetConfiguration/v2.0#ipv6
helpviewer_keywords:
- <ipv6> element
- ipv6 element
ms.assetid: 10b79aef-327b-4718-a892-e11f55e4d169
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 4b73e5d781829292513e809c39ac9de9dfc6d0e8
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32742482"
---
# <a name="ltipv6gt-element-network-settings"></a><span data-ttu-id="11a4c-102">&lt;IPv6&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="11a4c-102">&lt;ipv6&gt; Element (Network Settings)</span></span>
<span data-ttu-id="11a4c-103">Protocole Internet version 6 (IPv6) permet de réponses à partir des membres obsolètes de la <xref:System.Net.Dns> classe.</span><span class="sxs-lookup"><span data-stu-id="11a4c-103">Enables Internet Protocol version 6 (IPv6) responses from obsolete members of the <xref:System.Net.Dns> class.</span></span>  
  
 <span data-ttu-id="11a4c-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="11a4c-104">\<configuration></span></span>  
<span data-ttu-id="11a4c-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="11a4c-105">\<system.net></span></span>  
<span data-ttu-id="11a4c-106">\<Paramètres ></span><span class="sxs-lookup"><span data-stu-id="11a4c-106">\<settings></span></span>  
<span data-ttu-id="11a4c-107">\<IPv6 ></span><span class="sxs-lookup"><span data-stu-id="11a4c-107">\<ipv6></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11a4c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11a4c-108">Syntax</span></span>  
  
```xml  
<ipv6  
  enabled="true|false"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="11a4c-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="11a4c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="11a4c-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="11a4c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="11a4c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="11a4c-111">Attributes</span></span>  
  
|<span data-ttu-id="11a4c-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="11a4c-112">**Attribute**</span></span>|<span data-ttu-id="11a4c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="11a4c-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`enabled`|<span data-ttu-id="11a4c-114">Spécifie si les membres de la <xref:System.Net.Dns> classe retourner protocole Internet version 6 (IPv6) adresses.</span><span class="sxs-lookup"><span data-stu-id="11a4c-114">Specifies whether members of the <xref:System.Net.Dns> class return Internet Protocol version 6 (IPv6) addresses.</span></span> <span data-ttu-id="11a4c-115">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="11a4c-115">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="11a4c-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="11a4c-116">Child Elements</span></span>  
 <span data-ttu-id="11a4c-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="11a4c-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="11a4c-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="11a4c-118">Parent Elements</span></span>  
  
|<span data-ttu-id="11a4c-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="11a4c-119">**Element**</span></span>|<span data-ttu-id="11a4c-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="11a4c-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="11a4c-121">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11a4c-121">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="11a4c-122">Configure les options réseau de base pour l’espace de noms <xref:System.Net>.</span><span class="sxs-lookup"><span data-stu-id="11a4c-122">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="11a4c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="11a4c-123">Remarks</span></span>  
 <span data-ttu-id="11a4c-124">Ce paramètre permet la prise en charge IPv6 pour les membres obsolètes de la <xref:System.Net.Dns> classe : <xref:System.Net.Dns.BeginGetHostByName%2A>, <xref:System.Net.Dns.BeginResolve%2A>, <xref:System.Net.Dns.EndGetHostByName%2A>, <xref:System.Net.Dns.EndResolve%2A>, <xref:System.Net.Dns.GetHostByAddress%2A>, <xref:System.Net.Dns.GetHostByName%2A>, et <xref:System.Net.Dns.Resolve%2A>.</span><span class="sxs-lookup"><span data-stu-id="11a4c-124">This setting enables IPv6 support for the obsolete members of the <xref:System.Net.Dns> class: <xref:System.Net.Dns.BeginGetHostByName%2A>, <xref:System.Net.Dns.BeginResolve%2A>, <xref:System.Net.Dns.EndGetHostByName%2A>, <xref:System.Net.Dns.EndResolve%2A>, <xref:System.Net.Dns.GetHostByAddress%2A>, <xref:System.Net.Dns.GetHostByName%2A>, and <xref:System.Net.Dns.Resolve%2A>.</span></span> <span data-ttu-id="11a4c-125">Pour les autres membres de le <xref:System.Net?displayProperty=nameWithType> espace de noms, les adresses IPv6 peuvent être retournées si IPv6 est activé dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="11a4c-125">For other members of the <xref:System.Net?displayProperty=nameWithType> namespace, IPv6 addresses may be returned if IPv6 is enabled in the operating system.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="11a4c-126">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="11a4c-126">Configuration Files</span></span>  
 <span data-ttu-id="11a4c-127">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="11a4c-127">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="11a4c-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="11a4c-128">Example</span></span>  
 <span data-ttu-id="11a4c-129">L’exemple suivant montre comment activer la prise en charge IPv6 pour la <xref:System.Net.Dns> classe.</span><span class="sxs-lookup"><span data-stu-id="11a4c-129">The following example shows how to enable IPv6 support for the <xref:System.Net.Dns> class.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <ipv6 enabled="true"/>  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="11a4c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11a4c-130">See Also</span></span>  
 <xref:System.Net?displayProperty=nameWithType>  
 <xref:System.Net.Dns?displayProperty=nameWithType>  
 <xref:System.Net.Sockets.Socket.OSSupportsIPv6%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="11a4c-131">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="11a4c-131">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
