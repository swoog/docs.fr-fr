---
title: Configuration du proxy
ms.date: 06/18/2018
helpviewer_keywords:
- Networking
- adaptive proxies
- static proxies
- Network Resources
- Internet, proxy configuration
- proxies
- network, proxy configuration
- proxies, configuring
ms.assetid: 353c0a8b-4cee-44f6-8e65-60e286743df9
ms.openlocfilehash: c6b3808a2d73070cc07b31eb0fca7ca9d6af8cdb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59200543"
---
# <a name="proxy-configuration"></a><span data-ttu-id="9d53f-102">Configuration du proxy</span><span class="sxs-lookup"><span data-stu-id="9d53f-102">Proxy Configuration</span></span>
<span data-ttu-id="9d53f-103">Un serveur proxy gère les demandes du client pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="9d53f-103">A proxy server handles client requests for resources.</span></span> <span data-ttu-id="9d53f-104">Un proxy peut retourner une ressource demandée à partir de son cache ou transférer la demande au serveur sur lequel réside la ressource.</span><span class="sxs-lookup"><span data-stu-id="9d53f-104">A proxy can return a requested resource from its cache or forward the request to the server where the resource resides.</span></span> <span data-ttu-id="9d53f-105">Les proxies peuvent améliorer les performances réseau en réduisant le nombre de demandes envoyées aux serveurs distants.</span><span class="sxs-lookup"><span data-stu-id="9d53f-105">Proxies can improve network performance by reducing the number of requests sent to remote servers.</span></span> <span data-ttu-id="9d53f-106">Les proxies peuvent également être utilisés pour restreindre l'accès aux ressources.</span><span class="sxs-lookup"><span data-stu-id="9d53f-106">Proxies can also be used to restrict access to resources.</span></span>  
  
## <a name="adaptive-proxies"></a><span data-ttu-id="9d53f-107">Proxies adaptatifs</span><span class="sxs-lookup"><span data-stu-id="9d53f-107">Adaptive Proxies</span></span>  
 <span data-ttu-id="9d53f-108">Dans le .NET Framework, les proxies sont fournis sous deux formes : adaptatifs et statiques.</span><span class="sxs-lookup"><span data-stu-id="9d53f-108">In the .NET Framework, proxies come in two varieties: adaptive and static.</span></span> <span data-ttu-id="9d53f-109">Les proxies adaptatifs ajustent leurs paramètres lorsque la configuration du réseau change.</span><span class="sxs-lookup"><span data-stu-id="9d53f-109">Adaptive proxies adjust their settings when the network configuration changes.</span></span> <span data-ttu-id="9d53f-110">Par exemple, si l'utilisateur d'un ordinateur portable démarre une connexion réseau d'accès à distance, un proxy adaptatif identifie cette modification, détecte et exécute son nouveau script de configuration, et ajuste ses paramètres de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="9d53f-110">For example, if a laptop user starts a dialup network connection, an adaptive proxy would recognize this change, discover and run its new configuration script, and adjust its settings appropriately.</span></span>  
  
 <span data-ttu-id="9d53f-111">Les proxys adaptatifs sont configurés par un script de configuration (voir [Détection automatique de proxy](../../../docs/framework/network-programming/automatic-proxy-detection.md)).</span><span class="sxs-lookup"><span data-stu-id="9d53f-111">Adaptive proxies are configured by a configuration script (see [Automatic Proxy Detection](../../../docs/framework/network-programming/automatic-proxy-detection.md)).</span></span> <span data-ttu-id="9d53f-112">Le script génère un ensemble de protocoles d'application et un proxy pour chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="9d53f-112">The script generates a set of application protocols and a proxy for each protocol.</span></span>  
  
 <span data-ttu-id="9d53f-113">Les modifications apportées à l'environnement réseau peuvent nécessiter que le système utilise un nouvel ensemble de proxies.</span><span class="sxs-lookup"><span data-stu-id="9d53f-113">Changes in the network environment may require that the system use a new set of proxies.</span></span> <span data-ttu-id="9d53f-114">En cas de défaillance d'une connexion réseau ou d'initialisation d'une nouvelle connexion réseau, le système doit détecter la source appropriée du script de configuration dans le nouvel environnement et exécuter le nouveau script.</span><span class="sxs-lookup"><span data-stu-id="9d53f-114">If a network connection goes down or a new network connection is initialized, the system must discover the appropriate source of the configuration script in the new environment and run the new script.</span></span>  
  
 <span data-ttu-id="9d53f-115">Vous pouvez utiliser l’attribut `usesystemdefault` de l’élément [`<proxy>`](../configure-apps/file-schema/network/proxy-element-network-settings.md) dans votre fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d53f-115">You can use the `usesystemdefault` attribute of the [`<proxy>`](../configure-apps/file-schema/network/proxy-element-network-settings.md) element in your configuration file.</span></span> <span data-ttu-id="9d53f-116">L’attribut `usesystemdefault` détermine si les paramètres de proxy statiques (adresse de proxy, liste de contournement et contournement en local) doivent être lus à partir des paramètres de proxy Internet Explorer de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d53f-116">The `usesystemdefault` attribute controls whether the static proxy settings (proxy address, bypass list, and bypass on local) should be read from the Internet Explorer proxy settings for the user.</span></span> <span data-ttu-id="9d53f-117">S’il a la valeur `true`, les paramètres de proxy statiques Internet Explorer sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9d53f-117">If this value is set to `true`, the static proxy settings from Internet Explorer will be used.</span></span> <span data-ttu-id="9d53f-118">S’il a la valeur `false` ou s’il n’est pas défini, les paramètres de proxy statiques peuvent être spécifiés dans la configuration et remplacer les paramètres de proxy Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9d53f-118">If this value is `false` or not set, the static proxy settings can be specified in the configuration and will override the Internet Explorer proxy settings.</span></span> <span data-ttu-id="9d53f-119">En outre, cet attribut doit avoir la valeur `false` ou ne pas être défini pour que les proxys adaptatifs soient activés.</span><span class="sxs-lookup"><span data-stu-id="9d53f-119">This value must also be set to `false` or not set for adaptive proxies to be enabled.</span></span>  
  
 <span data-ttu-id="9d53f-120">L'exemple suivant illustre une configuration de proxy adaptatif classique.</span><span class="sxs-lookup"><span data-stu-id="9d53f-120">The following example shows a typical adaptive proxy configuration.</span></span>  
  
```xml  
<system.net>  
    <defaultProxy>  
      <proxy usesystemdefault="false" />
    </defaultProxy>  
</system.net>  
```  
  
## <a name="static-proxies"></a><span data-ttu-id="9d53f-121">Proxies statiques</span><span class="sxs-lookup"><span data-stu-id="9d53f-121">Static Proxies</span></span>  
 <span data-ttu-id="9d53f-122">Les proxies statiques sont généralement configurés explicitement par une application, ou lorsqu'un fichier de configuration est appelé par une application ou le système.</span><span class="sxs-lookup"><span data-stu-id="9d53f-122">Static proxies are usually configured explicitly by an application, or when a configuration file is invoked by an application or the system.</span></span> <span data-ttu-id="9d53f-123">Les proxies statiques sont utiles dans les réseaux dans lesquels la topologie change rarement, par exemple dans le cas d'un ordinateur de bureau connecté à un réseau d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="9d53f-123">Static proxies are useful in networks in which the topology changes infrequently, such as a desktop computer connected to a corporate network.</span></span>  
  
 <span data-ttu-id="9d53f-124">Plusieurs options déterminent le fonctionnement d'un proxy statique.</span><span class="sxs-lookup"><span data-stu-id="9d53f-124">Several options control how a static proxy operates.</span></span> <span data-ttu-id="9d53f-125">Spécifiez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d53f-125">You can specify the following:</span></span>  
  
-   <span data-ttu-id="9d53f-126">l'adresse du proxy ;</span><span class="sxs-lookup"><span data-stu-id="9d53f-126">The address of the proxy.</span></span>  
  
-   <span data-ttu-id="9d53f-127">si le proxy doit être ignoré pour les adresses locales ;</span><span class="sxs-lookup"><span data-stu-id="9d53f-127">Whether the proxy should be bypassed for local addresses.</span></span>  
  
-   <span data-ttu-id="9d53f-128">si le proxy doit être ignoré pour un ensemble d'adresses donné.</span><span class="sxs-lookup"><span data-stu-id="9d53f-128">Whether the proxy should be bypassed for a set of addresses.</span></span>  
  
 <span data-ttu-id="9d53f-129">Le tableau suivant présente les options de configuration d'un proxy statique.</span><span class="sxs-lookup"><span data-stu-id="9d53f-129">The following table shows the configuration options for a static proxy.</span></span>  
  
|<span data-ttu-id="9d53f-130">Attribut, propriété ou paramètre de fichier de configuration</span><span class="sxs-lookup"><span data-stu-id="9d53f-130">Attribute, property, or configuration file setting</span></span>|<span data-ttu-id="9d53f-131">Description</span><span class="sxs-lookup"><span data-stu-id="9d53f-131">Description</span></span>|  
|--------------------------------------------------------|-----------------|  
|`proxyaddress` <span data-ttu-id="9d53f-132">ou</span><span class="sxs-lookup"><span data-stu-id="9d53f-132">or</span></span> <xref:System.Net.WebProxy.Address>|<span data-ttu-id="9d53f-133">L'adresse du proxy à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9d53f-133">The address of the proxy to use.</span></span>|  
|`bypassonlocal` <span data-ttu-id="9d53f-134">ou</span><span class="sxs-lookup"><span data-stu-id="9d53f-134">or</span></span> <xref:System.Net.WebProxy.BypassProxyOnLocal>|<span data-ttu-id="9d53f-135">Détermine si le proxy est ignoré pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="9d53f-135">Controls whether the proxy is bypassed for local addresses.</span></span>|  
|`bypasslist` <span data-ttu-id="9d53f-136">ou</span><span class="sxs-lookup"><span data-stu-id="9d53f-136">or</span></span> <xref:System.Net.WebProxy.BypassArrayList>|<span data-ttu-id="9d53f-137">Décrit, avec des expressions régulières, un ensemble d'adresses qui ignorent le proxy.</span><span class="sxs-lookup"><span data-stu-id="9d53f-137">Describes, with regular expressions, a set of addresses that bypass the proxy.</span></span>|  
|`usesystemdefault`|<span data-ttu-id="9d53f-138">Détermine si les paramètres de proxy statiques (adresse de proxy, liste de contournement et contournement en local) doivent être lus depuis les paramètres de proxy Internet Explorer de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d53f-138">Controls whether the static proxy settings (proxy address, bypass list, and bypass on local) should be read from the Internet Explorer proxy settings for the user.</span></span> <span data-ttu-id="9d53f-139">Si cet attribut à la valeur `true`, les paramètres de proxy statiques Internet Explorer sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9d53f-139">If this value is set to `true`, then the static proxy settings from Internet Explorer will be used.</span></span> <span data-ttu-id="9d53f-140">Dans .NET Framework 2.0, quand cet attribut à la valeur `true`, les paramètres de proxy Internet Explorer ne sont pas remplacés par d’autres paramètres de proxy figurant dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d53f-140">On .NET Framework 2.0 when this value is set to `true`, the Internet Explorer proxy settings are not overridden by other proxy settings in the configuration file.</span></span> <span data-ttu-id="9d53f-141">Sur .NET Framework 1.1, les paramètres de proxy Internet Explorer peuvent être substituées par d'autres paramètres de proxy figurant dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="9d53f-141">On .NET Framework 1.1, the Internet Explorer proxy settings can be overridden by other proxy settings in the configuration file.</span></span><br /><br /> <span data-ttu-id="9d53f-142">Si cet attribut à la valeur `false` ou s’il n’est pas défini, les paramètres de proxy statiques peuvent être spécifiés dans la configuration et remplacer les paramètres de proxy Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9d53f-142">If this value is `false` or not set, then the static proxy settings can be specified in the configuration and will override the Internet Explorer proxy settings.</span></span> <span data-ttu-id="9d53f-143">En outre, cet attribut doit avoir la valeur `false` ou ne pas être défini pour que les proxys adaptatifs soient activés.</span><span class="sxs-lookup"><span data-stu-id="9d53f-143">This value must also be set to `false` or not set for adaptive proxies to be enabled.</span></span>|  
  
 <span data-ttu-id="9d53f-144">L'exemple suivant illustre une configuration de proxy statique classique.</span><span class="sxs-lookup"><span data-stu-id="9d53f-144">The following example shows a typical static proxy configuration.</span></span>  
  
```xml  
<system.net>  
    <defaultProxy>  
        <proxy  proxyaddress="http://proxy.contoso.com:3128"  
                bypassonlocal="true"  
        />  
        <bypasslist>  
            <add address="[a-z]+.blueyonderairlines.com$" />  
        </bypasslist>  
    </defaultProxy>  
</system.net>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9d53f-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d53f-145">See also</span></span>

- <xref:System.Net.WebProxy>
- <xref:System.Net.GlobalProxySelection>
- [<span data-ttu-id="9d53f-146">Détection automatique de proxy</span><span class="sxs-lookup"><span data-stu-id="9d53f-146">Automatic Proxy Detection</span></span>](../../../docs/framework/network-programming/automatic-proxy-detection.md)
