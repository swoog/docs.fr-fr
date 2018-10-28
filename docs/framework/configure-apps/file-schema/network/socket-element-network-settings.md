---
title: '&lt;socket&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/settings/socket
- http://schemas.microsoft.com/.NetConfiguration/v2.0#socket
helpviewer_keywords:
- <socket> element
- socket element
ms.assetid: 366c634c-7d16-478f-aedf-053eda94a1a0
ms.openlocfilehash: ff06fd6518e67020b4d67d4e081307b8e54bae85
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194694"
---
# <a name="ltsocketgt-element-network-settings"></a><span data-ttu-id="91944-102">&lt;socket&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="91944-102">&lt;socket&gt; Element (Network Settings)</span></span>
<span data-ttu-id="91944-103">Spécifie si les opérations de socket utilisent des ports de terminaison.</span><span class="sxs-lookup"><span data-stu-id="91944-103">Specifies whether socket operations use completion ports.</span></span>  
  
 <span data-ttu-id="91944-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="91944-104">\<configuration></span></span>  
<span data-ttu-id="91944-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="91944-105">\<system.net></span></span>  
<span data-ttu-id="91944-106">\<Paramètres ></span><span class="sxs-lookup"><span data-stu-id="91944-106">\<settings></span></span>  
<span data-ttu-id="91944-107">\<Socket ></span><span class="sxs-lookup"><span data-stu-id="91944-107">\<socket></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91944-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91944-108">Syntax</span></span>  
  
```xml  
<socket  
  alwaysUseCompletionPortsForConnect="true|false"  
  alwaysUseCompletionPortsForAccept="true|false"  
  ipProtectionLevel="EdgeRestricted|Restricted|Unrestricted|Unspecified"  
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="91944-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="91944-109">Attributes and Elements</span></span>  
 <span data-ttu-id="91944-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="91944-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="91944-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="91944-111">Attributes</span></span>  
  
|<span data-ttu-id="91944-112">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="91944-112">**Attribute**</span></span>|<span data-ttu-id="91944-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="91944-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`alwaysUseCompletionPortsForAccept`|<span data-ttu-id="91944-114">Indique si le socket doit toujours utiliser des ports de terminaison pour accepter les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="91944-114">Indicates whether the socket should always use completion ports for Accept method calls.</span></span> <span data-ttu-id="91944-115">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="91944-115">The default value is `false`.</span></span>|  
|`alwaysUseCompletionPortsForConnect`|<span data-ttu-id="91944-116">Indique si le socket doit toujours utiliser des ports de terminaison pour les appels de méthode Connect.</span><span class="sxs-lookup"><span data-stu-id="91944-116">Indicates whether the socket should always use completion ports for Connect method calls.</span></span> <span data-ttu-id="91944-117">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="91944-117">The default value is `false`.</span></span>|  
|`ipProtectionLevel`|<span data-ttu-id="91944-118">Spécifie la valeur par défaut <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> à utiliser pour un socket.</span><span class="sxs-lookup"><span data-stu-id="91944-118">Specifies the default <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> to use for a socket.</span></span> <span data-ttu-id="91944-119">La valeur par défaut dépend de la version de Windows.</span><span class="sxs-lookup"><span data-stu-id="91944-119">The default value depends on the version of Windows.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="91944-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="91944-120">Child Elements</span></span>  
 <span data-ttu-id="91944-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="91944-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="91944-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="91944-122">Parent Elements</span></span>  
  
|<span data-ttu-id="91944-123">**Élément**</span><span class="sxs-lookup"><span data-stu-id="91944-123">**Element**</span></span>|<span data-ttu-id="91944-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="91944-124">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="91944-125">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91944-125">settings</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/settings-element-network-settings.md)|<span data-ttu-id="91944-126">Configure les options réseau de base pour l’espace de noms <xref:System.Net>.</span><span class="sxs-lookup"><span data-stu-id="91944-126">Configures basic network options for the <xref:System.Net> namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="91944-127">Notes</span><span class="sxs-lookup"><span data-stu-id="91944-127">Remarks</span></span>  
 <span data-ttu-id="91944-128">Le `alwaysUseCompletionPortsForAccept` et `alwaysUseCompletionPortsForConnect` attributs sont utilisés pour spécifier le comportement par défaut concernant l’utilisation de ports de terminaison par les classes dans le <xref:System.Net.Sockets?displayProperty=nameWithType>.namespace.</span><span class="sxs-lookup"><span data-stu-id="91944-128">The `alwaysUseCompletionPortsForAccept` and `alwaysUseCompletionPortsForConnect` attributes are used to specify the default behavior regarding the use of completion ports by the classes in the <xref:System.Net.Sockets?displayProperty=nameWithType>.namespace.</span></span> <span data-ttu-id="91944-129">Ports de terminaison sont recommandés pour les applications de serveur hautes performances.</span><span class="sxs-lookup"><span data-stu-id="91944-129">Completion ports are recommended for high performance server applications.</span></span>  
  
 <span data-ttu-id="91944-130">La valeur par défaut pour le `alwaysUseCompletionPortsForAccept` et `alwaysUseCompletionPortsForConnect` attributs est **false**.</span><span class="sxs-lookup"><span data-stu-id="91944-130">The default value for the `alwaysUseCompletionPortsForAccept` and `alwaysUseCompletionPortsForConnect` attributes is **false**.</span></span>  
  
 <span data-ttu-id="91944-131">Le <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForAccept%2A> peut être utilisée pour obtenir la valeur actuelle de la `alwaysUseCompletionPortsForAccept` attribut à partir des fichiers de configuration applicables.</span><span class="sxs-lookup"><span data-stu-id="91944-131">The <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForAccept%2A> can be used to get the current value of the `alwaysUseCompletionPortsForAccept` attribute from applicable configuration files.</span></span> <span data-ttu-id="91944-132">Le <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForConnect%2A> peut être utilisée pour obtenir la valeur actuelle de la `alwaysUseCompletionPortsForConnect` attribut à partir des fichiers de configuration applicables.</span><span class="sxs-lookup"><span data-stu-id="91944-132">The <xref:System.Net.Configuration.SocketElement.AlwaysUseCompletionPortsForConnect%2A> can be used to get the current value of the `alwaysUseCompletionPortsForConnect` attribute from applicable configuration files.</span></span>  
  
 <span data-ttu-id="91944-133">Le `ipProtectionLevel` attribut spécifie la valeur par défaut <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> à utiliser pour un socket.</span><span class="sxs-lookup"><span data-stu-id="91944-133">The `ipProtectionLevel` attribute specifies the default <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> to use for a socket.</span></span> <span data-ttu-id="91944-134">Le <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> propriété permet la configuration d’une restriction pour un socket IPv6 à une portée spécifiée, telle que les adresses avec le même lien locales ou préfixe local de site.</span><span class="sxs-lookup"><span data-stu-id="91944-134">The <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> property enables configuration of a restriction for an IPv6 socket to a specified scope, such as addresses with the same link local or site local prefix.</span></span> <span data-ttu-id="91944-135">Cette option permet aux applications de placer des restrictions d’accès sur les sockets IPv6.</span><span class="sxs-lookup"><span data-stu-id="91944-135">This option enables applications to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="91944-136">Ces restrictions permettent à une application qui s'exécute sur un réseau local privé de se renforcer facilement et efficacement contre les attaques externes.</span><span class="sxs-lookup"><span data-stu-id="91944-136">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="91944-137">Cette option élargit ou limite la portée d’un socket d’écoute, permettant l’accès illimité des utilisateurs publics et privés le cas échéant, ou restreindre l’accès uniquement au même site, en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="91944-137">This option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>  
  
 <span data-ttu-id="91944-138">Cela `ipProtectionLevel` paramètre d’attribut affecte uniquement le trafic entrant initial :</span><span class="sxs-lookup"><span data-stu-id="91944-138">This `ipProtectionLevel` attribute setting affects only initial incoming traffic:</span></span>  
  
-   <span data-ttu-id="91944-139">Un serveur TCP à l’écoute les connexions entrantes sur un socket.</span><span class="sxs-lookup"><span data-stu-id="91944-139">A TCP server listening for incoming connections on a socket.</span></span>  
  
-   <span data-ttu-id="91944-140">Application UDP qui reçoit un paquet sur un socket.</span><span class="sxs-lookup"><span data-stu-id="91944-140">A UDP application receiving a packet on a socket.</span></span>  
  
 <span data-ttu-id="91944-141">Ce paramètre de configuration n’affecte pas les connexions TCP déjà établies (le trafic est illimité dans les deux directions) et n’affecte pas une application qui envoie des paquets UDP.</span><span class="sxs-lookup"><span data-stu-id="91944-141">This configuration setting does not affect already established TCP connections (traffic is unrestricted in both directions) and does not affect an application sending UDP packets.</span></span>  
  
 <span data-ttu-id="91944-142">Les valeurs possibles pour le `ipProtectionLevel` paramètre d’attribut correspondent aux niveaux de protection définis spécifiés dans le <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> énumération comme suit :</span><span class="sxs-lookup"><span data-stu-id="91944-142">The possible values for the `ipProtectionLevel` attribute setting correspond with the defined protection levels specified in the <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> enumeration as follows:</span></span>  
  
|<span data-ttu-id="91944-143">**Valeur d’attribut**</span><span class="sxs-lookup"><span data-stu-id="91944-143">**Attribute Value**</span></span>|<span data-ttu-id="91944-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="91944-144">**Description**</span></span>|  
|-|-|  
|<span data-ttu-id="91944-145">EdgeRestricted</span><span class="sxs-lookup"><span data-stu-id="91944-145">EdgeRestricted</span></span>|<span data-ttu-id="91944-146">Le niveau de protection IP est limité à un périmètre.</span><span class="sxs-lookup"><span data-stu-id="91944-146">The IP protection level is edge restricted.</span></span> <span data-ttu-id="91944-147">Cette valeur peut être utilisée par les applications conçues pour fonctionner sur Internet.</span><span class="sxs-lookup"><span data-stu-id="91944-147">This value would be used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="91944-148">Ce paramètre n’autorise pas de parcours de traduction d’adresses réseau (NAT) à l’aide de l’implémentation de Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="91944-148">This setting does not allow Network Address Translation (NAT) traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="91944-149">Ces applications peuvent contourner les pare-feux IPv4, applications ; doivent donc être renforcées contre les attaques Internet dirigées vers le port ouvert.</span><span class="sxs-lookup"><span data-stu-id="91944-149">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span> <span data-ttu-id="91944-150">Sur Windows Server 2003 et Windows XP, la valeur par défaut pour le niveau de Protection IP sur un socket est périmètre limité.</span><span class="sxs-lookup"><span data-stu-id="91944-150">On Windows Server 2003 and Windows XP, the default value for the IP Protection level on a socket is edge restricted.</span></span>|  
|<span data-ttu-id="91944-151">restreint</span><span class="sxs-lookup"><span data-stu-id="91944-151">Restricted</span></span>|<span data-ttu-id="91944-152">Le niveau de protection IP est limité.</span><span class="sxs-lookup"><span data-stu-id="91944-152">The IP protection level is restricted.</span></span> <span data-ttu-id="91944-153">Cette valeur peut être utilisée par les applications intranet qui n’implémentent pas de scénarios Internet.</span><span class="sxs-lookup"><span data-stu-id="91944-153">This value would be used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="91944-154">Ces applications sont généralement pas testées ou renforcées contre les attaques Internet.</span><span class="sxs-lookup"><span data-stu-id="91944-154">These applications are generally not tested or hardened against Internet-style attacks.</span></span> <span data-ttu-id="91944-155">Ce paramètre limite le trafic reçu aux liens locaux uniquement.</span><span class="sxs-lookup"><span data-stu-id="91944-155">This setting will limit the received traffic to link-local only.</span></span>|  
|<span data-ttu-id="91944-156">Non restreint</span><span class="sxs-lookup"><span data-stu-id="91944-156">Unrestricted</span></span>|<span data-ttu-id="91944-157">Le niveau de protection IP est illimité.</span><span class="sxs-lookup"><span data-stu-id="91944-157">The IP protection level is unrestricted.</span></span> <span data-ttu-id="91944-158">Cette valeur peut être utilisée par les applications conçues pour fonctionner sur Internet, notamment les applications qui tirent parti des fonctions de traversée NAT IPv6 intégrées à Windows (Teredo, par exemple).</span><span class="sxs-lookup"><span data-stu-id="91944-158">This value would be used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="91944-159">Ces applications peuvent contourner les pare-feux IPv4, applications ; doivent donc être renforcées contre les attaques Internet dirigées vers le port ouvert.</span><span class="sxs-lookup"><span data-stu-id="91944-159">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span> <span data-ttu-id="91944-160">Sur Windows Server 2008 R2 et Windows Vista, la valeur par défaut pour le niveau de Protection IP sur un socket est illimitée.</span><span class="sxs-lookup"><span data-stu-id="91944-160">On Windows Server 2008 R2 and Windows Vista, the default value for the IP Protection level on a socket is unrestricted.</span></span>|  
|<span data-ttu-id="91944-161">Non spécifié</span><span class="sxs-lookup"><span data-stu-id="91944-161">Unspecified</span></span>|<span data-ttu-id="91944-162">Le niveau de protection IP n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="91944-162">The IP protection level is unspecified.</span></span> <span data-ttu-id="91944-163">Sur Windows 7 et Windows Server 2008 R2, la valeur par défaut pour le niveau de Protection IP sur un socket n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="91944-163">On Windows 7 and Windows Server 2008 R2, the default value for the IP Protection level on a socket is unspecified.</span></span>|  
  
 <span data-ttu-id="91944-164">La valeur par défaut pour le `ipProtectionLevel` attribut est **Unspecified**.</span><span class="sxs-lookup"><span data-stu-id="91944-164">The default value for the `ipProtectionLevel` attribute is **Unspecified**.</span></span>  
  
 <span data-ttu-id="91944-165">Le <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> propriété peut être utilisée pour obtenir la valeur actuelle de la `ipProtectionLevel` attribut à partir des fichiers de configuration applicables.</span><span class="sxs-lookup"><span data-stu-id="91944-165">The <xref:System.Net.Configuration.SocketElement.IPProtectionLevel%2A> property can be used to get the current value of the `ipProtectionLevel` attribute from applicable configuration files.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="91944-166">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="91944-166">Configuration Files</span></span>  
 <span data-ttu-id="91944-167">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="91944-167">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="91944-168">Exemple</span><span class="sxs-lookup"><span data-stu-id="91944-168">Example</span></span>  
 <span data-ttu-id="91944-169">L’exemple suivant montre comment spécifier que les ports de terminaison doivent être utilisés et que la valeur par défaut <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> doit être illimité.</span><span class="sxs-lookup"><span data-stu-id="91944-169">The following example shows how to specify that completion ports should be used and that the default <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType> should be unrestricted.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <settings>  
      <socket  
        alwaysUseCompletionPortsForAccept="true"  
        alwaysUseCompletionPortsForConnect="true"  
        ipProtectionLevel="Unrestricted"  
       />  
    </settings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="91944-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91944-170">See Also</span></span>  
- <xref:System.Net?displayProperty=nameWithType>  
- <xref:System.Net.Configuration.SocketElement?displayProperty=nameWithType>  
- <xref:System.Net.Sockets?displayProperty=nameWithType>  
- <xref:System.Net.Sockets.IPProtectionLevel?displayProperty=nameWithType>  
- <xref:System.Net.Sockets.SocketOptionName.IPProtectionLevel?displayProperty=nameWithType>  
- [<span data-ttu-id="91944-171">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="91944-171">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
