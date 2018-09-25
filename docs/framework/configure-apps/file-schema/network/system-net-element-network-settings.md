---
title: '&lt;system.Net&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#system.Net
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.Net
helpviewer_keywords:
- system.Net element
- <system.Net> element
ms.assetid: 52de4d6c-b24d-44aa-ba7d-6b5061f1357e
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 25663774c639e9fea13ced54a9aa7f456922fa1a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47085687"
---
# <a name="ltsystemnetgt-element-network-settings"></a><span data-ttu-id="79e78-102">&lt;system.Net&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="79e78-102">&lt;system.Net&gt; Element (Network Settings)</span></span>
<span data-ttu-id="79e78-103">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="79e78-103">Contains settings that specify how the .NET Framework connects to the network.</span></span>  
  
 <span data-ttu-id="79e78-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="79e78-104">\<configuration></span></span>  
<span data-ttu-id="79e78-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="79e78-105">\<system.net></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79e78-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79e78-106">Syntax</span></span>  
  
```xml  
<system.net>   
</system.net>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="79e78-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="79e78-107">Attributes and Elements</span></span>  
 <span data-ttu-id="79e78-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="79e78-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="79e78-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="79e78-109">Attributes</span></span>  
 <span data-ttu-id="79e78-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="79e78-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="79e78-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="79e78-111">Child Elements</span></span>  
  
|<span data-ttu-id="79e78-112">**Élément**</span><span class="sxs-lookup"><span data-stu-id="79e78-112">**Element**</span></span>|<span data-ttu-id="79e78-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="79e78-113">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="79e78-114">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="79e78-114">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="79e78-115">Spécifie les modules utilisés pour authentifier les demandes Internet.</span><span class="sxs-lookup"><span data-stu-id="79e78-115">Specifies modules used to authenticate Internet requests.</span></span>|  
|[<span data-ttu-id="79e78-116">connectionManagement</span><span class="sxs-lookup"><span data-stu-id="79e78-116">connectionManagement</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/connectionmanagement-element-network-settings.md)|<span data-ttu-id="79e78-117">Spécifie le nombre maximal de connexions à un hôte Internet.</span><span class="sxs-lookup"><span data-stu-id="79e78-117">Specifies the maximum number of connections to an Internet host.</span></span>|  
|[<span data-ttu-id="79e78-118">defaultProxy</span><span class="sxs-lookup"><span data-stu-id="79e78-118">defaultProxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/defaultproxy-element-network-settings.md)|<span data-ttu-id="79e78-119">Configure le serveur proxy HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="79e78-119">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>|  
|[<span data-ttu-id="79e78-120">mailSettings</span><span class="sxs-lookup"><span data-stu-id="79e78-120">mailSettings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/mailsettings-element-network-settings.md)|<span data-ttu-id="79e78-121">Configure les options d’envoi du courrier SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="79e78-121">Configures Simple Mail Transport Protocol (SMTP) mail sending options.</span></span>|  
|[<span data-ttu-id="79e78-122">requestCaching</span><span class="sxs-lookup"><span data-stu-id="79e78-122">requestCaching</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)|<span data-ttu-id="79e78-123">Contrôle le mécanisme de mise en cache pour les demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="79e78-123">Controls the caching mechanism for network requests.</span></span>|  
|[<span data-ttu-id="79e78-124">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79e78-124">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="79e78-125">Configure les options réseau de base pour les classes dans le <xref:System.Net> et les espaces de noms enfants.</span><span class="sxs-lookup"><span data-stu-id="79e78-125">Configures basic network options for classes in the <xref:System.Net> and related child namespaces.</span></span>|  
|[<span data-ttu-id="79e78-126">webRequestModules</span><span class="sxs-lookup"><span data-stu-id="79e78-126">webRequestModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|<span data-ttu-id="79e78-127">Spécifie les modules à utiliser pour demander des informations à partir d’hôtes Internet.</span><span class="sxs-lookup"><span data-stu-id="79e78-127">Specifies modules to use to request information from Internet hosts.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="79e78-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="79e78-128">Parent Elements</span></span>  
  
|<span data-ttu-id="79e78-129">**Élément**</span><span class="sxs-lookup"><span data-stu-id="79e78-129">**Element**</span></span>|<span data-ttu-id="79e78-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="79e78-130">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="79e78-131">Configuration</span><span class="sxs-lookup"><span data-stu-id="79e78-131">configuration</span></span>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|<span data-ttu-id="79e78-132">Contient des paramètres pour tous les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="79e78-132">Contains settings for all namespaces.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="79e78-133">Notes</span><span class="sxs-lookup"><span data-stu-id="79e78-133">Remarks</span></span>  
 <span data-ttu-id="79e78-134">Le [ \<system.net >](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md) élément contient des paramètres pour les classes dans le <xref:System.Net> et les espaces de noms enfants.</span><span class="sxs-lookup"><span data-stu-id="79e78-134">The [\<system.net>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md) element contains settings for classes in the <xref:System.Net> and related child namespaces.</span></span> <span data-ttu-id="79e78-135">Les paramètres configurent les modules d’authentification, gestion des connexions, les paramètres de messagerie, le serveur proxy et les modules de demande Internet pour recevoir des informations à partir d’hôtes Internet.</span><span class="sxs-lookup"><span data-stu-id="79e78-135">The settings configure authentication modules, connection management, mail settings, the proxy server, and Internet request modules for receiving information from Internet hosts.</span></span>  
  
## <a name="example"></a><span data-ttu-id="79e78-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="79e78-136">Example</span></span>  
 <span data-ttu-id="79e78-137">L’exemple suivant montre une configuration classique utilisée par <xref:System.Net> classes.</span><span class="sxs-lookup"><span data-stu-id="79e78-137">The following example shows a typical configuration used by <xref:System.Net> classes.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <add type="System.Net.DigestClient" />  
      <add type="System.Net.NegotiateClient" />  
      <add type="System.Net.KerberosClient" />  
      <add type="System.Net.NtlmClient" />  
      <add type="System.Net.BasicClient" />  
    </authenticationModules>  
    <connectionManagement>  
      <add address="*" maxconnection="2" />  
    </connectionManagement>  
    <defaultProxy>  
      <proxy  
        usesystemdefault="true"  
        bypassonlocal="true"  
      />  
    </defaultProxy>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator"  
      />  
      <add prefix="https"  
           type="System.Net.HttpRequestCreator"  
      />  
      <add prefix="file"  
           type="System.Net.FileWebRequestCreator"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="79e78-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79e78-138">See Also</span></span>  
 [<span data-ttu-id="79e78-139">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="79e78-139">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
