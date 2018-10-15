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
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 1736dd8fcb308bceee5f100149919ff9ec45510d
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49316322"
---
# <a name="ltconnectionmanagementgt-element-network-settings"></a><span data-ttu-id="d9cda-102">&lt;connectionManagement&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="d9cda-102">&lt;connectionManagement&gt; Element (Network Settings)</span></span>
<span data-ttu-id="d9cda-103">Spécifie le nombre maximal de connexions à un hôte réseau.</span><span class="sxs-lookup"><span data-stu-id="d9cda-103">Specifies the maximum number of connections to a network host.</span></span>  
  
 <span data-ttu-id="d9cda-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d9cda-104">\<configuration></span></span>  
<span data-ttu-id="d9cda-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="d9cda-105">\<system.net></span></span>  
<span data-ttu-id="d9cda-106">\<connectionManagement ></span><span class="sxs-lookup"><span data-stu-id="d9cda-106">\<connectionManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9cda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9cda-107">Syntax</span></span>  
  
```xml  
<connectionManagement>   
</connectionManagement>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d9cda-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d9cda-108">Attributes and Elements</span></span>  
 <span data-ttu-id="d9cda-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d9cda-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d9cda-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d9cda-110">Attributes</span></span>  
 <span data-ttu-id="d9cda-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d9cda-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d9cda-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d9cda-112">Child Elements</span></span>  
  
|<span data-ttu-id="d9cda-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d9cda-113">**Element**</span></span>|<span data-ttu-id="d9cda-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="d9cda-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d9cda-115">add</span><span class="sxs-lookup"><span data-stu-id="d9cda-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="d9cda-116">Ajoute une adresse IP ou un nom DNS à la liste de gestion des connexions.</span><span class="sxs-lookup"><span data-stu-id="d9cda-116">Adds an IP address or DNS name to the connection management list.</span></span>|  
|[<span data-ttu-id="d9cda-117">clear</span><span class="sxs-lookup"><span data-stu-id="d9cda-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="d9cda-118">Efface la liste de gestion des connexions.</span><span class="sxs-lookup"><span data-stu-id="d9cda-118">Clears the connection management list.</span></span>|  
|[<span data-ttu-id="d9cda-119">remove</span><span class="sxs-lookup"><span data-stu-id="d9cda-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-connectionmanagement-network-settings.md)|<span data-ttu-id="d9cda-120">Supprime une adresse IP ou le nom DNS de la liste de gestion de connexion.</span><span class="sxs-lookup"><span data-stu-id="d9cda-120">Removes an IP address or DNS name from the connection management list.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d9cda-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d9cda-121">Parent Elements</span></span>  
  
|<span data-ttu-id="d9cda-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d9cda-122">**Element**</span></span>|<span data-ttu-id="d9cda-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="d9cda-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="d9cda-124">System.NET</span><span class="sxs-lookup"><span data-stu-id="d9cda-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="d9cda-125">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="d9cda-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d9cda-126">Notes</span><span class="sxs-lookup"><span data-stu-id="d9cda-126">Remarks</span></span>  
 <span data-ttu-id="d9cda-127">Le `connectionManagement` élément définit le nombre maximal de connexions sur un serveur ou un groupe de serveurs.</span><span class="sxs-lookup"><span data-stu-id="d9cda-127">The `connectionManagement` element defines the maximum number of connections to a server or group of servers.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="d9cda-128">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="d9cda-128">Configuration Files</span></span>  
 <span data-ttu-id="d9cda-129">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="d9cda-129">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d9cda-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9cda-130">Example</span></span>  
 <span data-ttu-id="d9cda-131">L’exemple suivant configure une application d’utiliser quatre connexions au serveur `www.contoso.com` et deux connexions à tous les autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="d9cda-131">The following example configures an application to use four connections to the server `www.contoso.com` and two connections to all other servers.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="d9cda-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9cda-132">See Also</span></span>  
 <xref:System.Net.ServicePoint>  
 <xref:System.Net.ServicePointManager>  
 [<span data-ttu-id="d9cda-133">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="d9cda-133">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
