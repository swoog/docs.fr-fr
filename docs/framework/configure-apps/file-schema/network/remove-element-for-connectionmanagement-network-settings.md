---
title: <remove> Élément de connectionManagement (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/connectionManagement/remove
- http://schemas.microsoft.com/.NetConfiguration/v2.0#remove
helpviewer_keywords:
- connectionManagement, remove element
- <remove> element, connectionManagement
- <connectionManagement>, remove element
- remove element, connectionManagement
ms.assetid: 94b81775-5a22-4975-8c47-8620c40c3f35
ms.openlocfilehash: d9c584fb2faa971e7ce1ca287a94c8c6129820fd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59158858"
---
# <a name="remove-element-for-connectionmanagement-network-settings"></a><span data-ttu-id="ac3d8-102">\<Supprimer >, élément de connectionManagement (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="ac3d8-102">\<remove> Element for connectionManagement (Network Settings)</span></span>
<span data-ttu-id="ac3d8-103">Supprime une adresse IP ou le nom DNS de la liste de gestion de connexion.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-103">Removes an IP address or DNS name from the connection management list.</span></span>  
  
 <span data-ttu-id="ac3d8-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ac3d8-104">\<configuration></span></span>  
<span data-ttu-id="ac3d8-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="ac3d8-105">\<system.net></span></span>  
<span data-ttu-id="ac3d8-106">\<connectionManagement></span><span class="sxs-lookup"><span data-stu-id="ac3d8-106">\<connectionManagement></span></span>  
<span data-ttu-id="ac3d8-107">\<remove></span><span class="sxs-lookup"><span data-stu-id="ac3d8-107">\<remove></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac3d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac3d8-108">Syntax</span></span>  
  
```xml  
<remove   
  address="server name or IP address"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ac3d8-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ac3d8-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ac3d8-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ac3d8-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ac3d8-111">Attributes</span></span>  
  
|**<span data-ttu-id="ac3d8-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ac3d8-112">Attribute</span></span>**|**<span data-ttu-id="ac3d8-113">Description</span><span class="sxs-lookup"><span data-stu-id="ac3d8-113">Description</span></span>**|  
|-------------------|---------------------|  
|`address`|<span data-ttu-id="ac3d8-114">Une adresse IP ou le nom DNS.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-114">An IP address or DNS name.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ac3d8-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ac3d8-115">Child Elements</span></span>  
 <span data-ttu-id="ac3d8-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ac3d8-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ac3d8-117">Parent Elements</span></span>  
  
|**<span data-ttu-id="ac3d8-118">Élément</span><span class="sxs-lookup"><span data-stu-id="ac3d8-118">Element</span></span>**|**<span data-ttu-id="ac3d8-119">Description</span><span class="sxs-lookup"><span data-stu-id="ac3d8-119">Description</span></span>**|  
|-----------------|---------------------|  
|[<span data-ttu-id="ac3d8-120">connectionManagement</span><span class="sxs-lookup"><span data-stu-id="ac3d8-120">connectionManagement</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/connectionmanagement-element-network-settings.md)|<span data-ttu-id="ac3d8-121">Spécifie le nombre maximal de connexions à un hôte réseau.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-121">Specifies the maximum number of connections to a network host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ac3d8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ac3d8-122">Remarks</span></span>  
 <span data-ttu-id="ac3d8-123">Le `remove` élément supprime l’entrée de liste de gestion de connexion pour le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-123">The `remove` element removes the connection management list entry for the specified server.</span></span>  
  
 <span data-ttu-id="ac3d8-124">La valeur de la `address` attribut doit être un nom d’hôte ou adresse IP valide.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-124">The value of the `address` attribute should be a valid IP address or host name.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="ac3d8-125">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="ac3d8-125">Configuration Files</span></span>  
 <span data-ttu-id="ac3d8-126">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="ac3d8-126">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ac3d8-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="ac3d8-127">Example</span></span>  
 <span data-ttu-id="ac3d8-128">L’exemple suivant supprime les entrées de liste de gestion connexion pour le serveur `www.adventure-works.com` , puis configure une application d’utiliser quatre connexions au serveur `www.contoso.com` et deux connexions à tous les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="ac3d8-128">The following example removes any connection management list entries for the server `www.adventure-works.com` and then configures an application to use four connections to the server `www.contoso.com` and two connections to all other servers.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <connectionManagement>  
      <remove address="http://www.adventure-works.com" />  
      <add address="http://www.contoso.com" maxconnection="4" />  
      <add address="*" maxconnection="2" />  
    </connectionManagement>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ac3d8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac3d8-129">See also</span></span>

- <xref:System.Net.ServicePoint>
- <xref:System.Net.ServicePointManager>
- [<span data-ttu-id="ac3d8-130">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="ac3d8-130">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
