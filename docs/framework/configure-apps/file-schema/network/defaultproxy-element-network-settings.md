---
title: '&lt;defaultProxy&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#defaultProxy
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/defaultProxy
helpviewer_keywords:
- defaultProxy element
- <defaultProxy> element
ms.assetid: 9d663c4b-07b4-4f6f-9b12-efbd3630354f
ms.openlocfilehash: 48c5f5a50563cdbea5fa806e7c7524e413ba3712
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54596174"
---
# <a name="ltdefaultproxygt-element-network-settings"></a><span data-ttu-id="62a8a-102">&lt;defaultProxy&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="62a8a-102">&lt;defaultProxy&gt; Element (Network Settings)</span></span>
<span data-ttu-id="62a8a-103">Configure le serveur proxy HTTP (Hypertext Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="62a8a-103">Configures the Hypertext Transfer Protocol (HTTP) proxy server.</span></span>  
  
 <span data-ttu-id="62a8a-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="62a8a-104">\<configuration></span></span>  
<span data-ttu-id="62a8a-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="62a8a-105">\<system.net></span></span>  
<span data-ttu-id="62a8a-106">\<defaultProxy></span><span class="sxs-lookup"><span data-stu-id="62a8a-106">\<defaultProxy></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62a8a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62a8a-107">Syntax</span></span>  
  
```xml  
<defaultProxy  
  enabled="true|false"  
  useDefaultCredentials="true|false">  
    <bypasslist>...</bypasslist>  
    <proxy>...</proxy>  
    <module>...</module>  
</defaultProxy>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="62a8a-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="62a8a-108">Attributes and Elements</span></span>  
 <span data-ttu-id="62a8a-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="62a8a-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="62a8a-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="62a8a-110">Attributes</span></span>  
  
|<span data-ttu-id="62a8a-111">**Élément**</span><span class="sxs-lookup"><span data-stu-id="62a8a-111">**Element**</span></span>|<span data-ttu-id="62a8a-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="62a8a-112">**Description**</span></span>|  
|-----------------|---------------------|  
|`enabled`|<span data-ttu-id="62a8a-113">Spécifie si un proxy web est utilisé.</span><span class="sxs-lookup"><span data-stu-id="62a8a-113">Specifies whether a web proxy is used.</span></span> <span data-ttu-id="62a8a-114">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="62a8a-114">The default value is `true`.</span></span>|  
|`useDefaultCredentials`|<span data-ttu-id="62a8a-115">Spécifie si les informations d'identification par défaut associées à cet hôte sont utilisées pour accéder au proxy web.</span><span class="sxs-lookup"><span data-stu-id="62a8a-115">Specifies whether the default credentials for this host are used to access the web proxy.</span></span> <span data-ttu-id="62a8a-116">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="62a8a-116">The default value is `false`.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="62a8a-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="62a8a-117">Child Elements</span></span>  
  
|<span data-ttu-id="62a8a-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="62a8a-118">**Element**</span></span>|<span data-ttu-id="62a8a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="62a8a-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="62a8a-120">bypasslist</span><span class="sxs-lookup"><span data-stu-id="62a8a-120">bypasslist</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/bypasslist-element-network-settings.md)|<span data-ttu-id="62a8a-121">Fournit un ensemble d'expressions régulières décrivant les adresses qui n'utilisent pas le proxy.</span><span class="sxs-lookup"><span data-stu-id="62a8a-121">Provides a set of regular expressions that describe addresses that do not use the proxy.</span></span>|  
|[<span data-ttu-id="62a8a-122">module</span><span class="sxs-lookup"><span data-stu-id="62a8a-122">module</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/module-element-network-settings.md)|<span data-ttu-id="62a8a-123">Ajoute un nouveau module proxy à l'application.</span><span class="sxs-lookup"><span data-stu-id="62a8a-123">Adds a new proxy module to the application.</span></span>|  
|[<span data-ttu-id="62a8a-124">proxy</span><span class="sxs-lookup"><span data-stu-id="62a8a-124">proxy</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/proxy-element-network-settings.md)|<span data-ttu-id="62a8a-125">Définit un serveur proxy.</span><span class="sxs-lookup"><span data-stu-id="62a8a-125">Defines a proxy server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="62a8a-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="62a8a-126">Parent Elements</span></span>  
  
|<span data-ttu-id="62a8a-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="62a8a-127">**Element**</span></span>|<span data-ttu-id="62a8a-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="62a8a-128">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="62a8a-129">system.net</span><span class="sxs-lookup"><span data-stu-id="62a8a-129">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="62a8a-130">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="62a8a-130">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62a8a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="62a8a-131">Remarks</span></span>  
 <span data-ttu-id="62a8a-132">Si l'élément defaultProxy est vide, les paramètres du proxy Internet Explorer sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="62a8a-132">If the defaultProxy element is empty, the proxy settings from Internet Explorer will be used.</span></span> <span data-ttu-id="62a8a-133">Ce comportement est différent de la version 1.1 de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="62a8a-133">This behavior is different from version 1.1 of the .NET Framework.</span></span>  
  
 <span data-ttu-id="62a8a-134">Une exception est levée si le [module](../../../../../docs/framework/configure-apps/file-schema/network/module-element-network-settings.md) élément spécifie un type non public, le type ne dérive pas de la <xref:System.Net.IWebProxy> (classe), une exception à partir du constructeur par défaut de cet objet s’est produite, ou une exception s’est produite alors que récupération du proxy système spécifié la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="62a8a-134">An exception is thrown if the [module](../../../../../docs/framework/configure-apps/file-schema/network/module-element-network-settings.md) element specifies a non-public type, the type is not deriving from the <xref:System.Net.IWebProxy> class, an exception from the default constructor of this object occurred, or an exception occurred while retrieving the system-specified default proxy.</span></span> <span data-ttu-id="62a8a-135">La propriété <xref:System.Exception.InnerException%2A> de l’exception fournit normalement plus d’informations sur la cause racine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="62a8a-135">The <xref:System.Exception.InnerException%2A> property on the exception should have more information about the root cause of the error.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="62a8a-136">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="62a8a-136">Configuration Files</span></span>  
 <span data-ttu-id="62a8a-137">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="62a8a-137">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="62a8a-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="62a8a-138">Example</span></span>  
 <span data-ttu-id="62a8a-139">L’exemple suivant utilise les valeurs par défaut du proxy Internet Explorer, spécifie l’adresse de proxy et contourne le proxy pour un accès local et contoso.com.</span><span class="sxs-lookup"><span data-stu-id="62a8a-139">The following example uses the defaults from the Internet Explorer proxy, specifies the proxy address, and bypasses the proxy for local access and contoso.com.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <defaultProxy>  
      <proxy  
        usesystemdefault="true"  
        proxyaddress="http://192.168.1.10:3128"  
        bypassonlocal="true"  
      />  
      <bypasslist>  
        <add address="[a-z]+\.contoso\.com$" />  
      </bypasslist>  
    </defaultProxy>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="62a8a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62a8a-140">See also</span></span>
- <xref:System.Net.WebProxy?displayProperty=nameWithType>
- [<span data-ttu-id="62a8a-141">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="62a8a-141">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
