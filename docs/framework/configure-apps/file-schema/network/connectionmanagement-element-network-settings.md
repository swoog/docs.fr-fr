---
title: '&lt;connectionManagement&gt; , élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/connectionManagement
- http://schemas.microsoft.com/.NetConfiguration/v2.0#connectionManagement
helpviewer_keywords:
- <connectionManagement> element
- connectionManagement element
ms.assetid: bedccaab-12a2-4511-8f67-e961f249aec6
ms.openlocfilehash: ff2f895ca50f0d16ee9e16406f92b087b03e391e
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/26/2018
ms.locfileid: "50049111"
---
# <a name="ltconnectionmanagementgt-element-network-settings"></a><span data-ttu-id="91ab8-102">&lt;connectionManagement&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="91ab8-102">&lt;connectionManagement&gt; Element (Network Settings)</span></span>
<span data-ttu-id="91ab8-103">Spécifie le nombre maximal de connexions à un hôte réseau.</span><span class="sxs-lookup"><span data-stu-id="91ab8-103">Specifies the maximum number of connections to a network host.</span></span>  
  
 <span data-ttu-id="91ab8-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="91ab8-104">\<configuration></span></span>  
<span data-ttu-id="91ab8-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="91ab8-105">\<system.net></span></span>  
<span data-ttu-id="91ab8-106">\<connectionManagement ></span><span class="sxs-lookup"><span data-stu-id="91ab8-106">\<connectionManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91ab8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91ab8-107">Syntax</span></span>  
  
```xml  
<connectionManagement>   
</connectionManagement>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="91ab8-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="91ab8-108">Attributes and Elements</span></span>  
 <span data-ttu-id="91ab8-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="91ab8-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="91ab8-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="91ab8-110">Attributes</span></span>  
 <span data-ttu-id="91ab8-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="91ab8-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="91ab8-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="91ab8-112">Child Elements</span></span>  
  
|<span data-ttu-id="91ab8-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="91ab8-113">**Element**</span></span>|<span data-ttu-id="91ab8-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="91ab8-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="91ab8-115">add</span><span class="sxs-lookup"><span data-stu-id="91ab8-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="91ab8-116">Ajoute une adresse IP ou un nom DNS à la liste de gestion des connexions.</span><span class="sxs-lookup"><span data-stu-id="91ab8-116">Adds an IP address or DNS name to the connection management list.</span></span>|  
|[<span data-ttu-id="91ab8-117">clear</span><span class="sxs-lookup"><span data-stu-id="91ab8-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="91ab8-118">Efface la liste de gestion des connexions.</span><span class="sxs-lookup"><span data-stu-id="91ab8-118">Clears the connection management list.</span></span>|  
|[<span data-ttu-id="91ab8-119">remove</span><span class="sxs-lookup"><span data-stu-id="91ab8-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="91ab8-120">Supprime une adresse IP ou le nom DNS de la liste de gestion de connexion.</span><span class="sxs-lookup"><span data-stu-id="91ab8-120">Removes an IP address or DNS name from the connection management list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="91ab8-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="91ab8-121">Parent Elements</span></span>  
  
|<span data-ttu-id="91ab8-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="91ab8-122">**Element**</span></span>|<span data-ttu-id="91ab8-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="91ab8-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="91ab8-124">System.NET</span><span class="sxs-lookup"><span data-stu-id="91ab8-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="91ab8-125">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="91ab8-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="91ab8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="91ab8-126">Remarks</span></span>  
 <span data-ttu-id="91ab8-127">Le `connectionManagement` élément définit le nombre maximal de connexions sur un serveur ou un groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="91ab8-127">The `connectionManagement` element defines the maximum number of connections to a server or group of servers.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="91ab8-128">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="91ab8-128">Configuration Files</span></span>  
 <span data-ttu-id="91ab8-129">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="91ab8-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="91ab8-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="91ab8-130">Example</span></span>  
 <span data-ttu-id="91ab8-131">L’exemple suivant configure une application d’utiliser quatre connexions au serveur `www.contoso.com` et deux connexions à tous les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="91ab8-131">The following example configures an application to use four connections to the server `www.contoso.com` and two connections to all other servers.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <connectionManagement>  
      <add address = "http://www.contoso.com" maxconnection = "4" />  
      <add address = "*" maxconnection = "2" />  
    </connectionManagement>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="91ab8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91ab8-132">See Also</span></span>  
 <xref:System.Net.ServicePoint>  
 <xref:System.Net.ServicePointManager>  
 [<span data-ttu-id="91ab8-133">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="91ab8-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
