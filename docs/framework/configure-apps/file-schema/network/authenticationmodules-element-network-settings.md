---
title: '&lt;authenticationModules&gt; élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#authenticationModules
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules
helpviewer_keywords:
- authenticationModules element
- <authenticationModules> element
ms.assetid: 10fcfaad-82ef-4692-871a-0aec9dfbe75e
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 6d7f811a5746fa07264a192efdc4c5c02323e1f4
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltauthenticationmodulesgt-element-network-settings"></a><span data-ttu-id="7d014-102">&lt;authenticationModules&gt; élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="7d014-102">&lt;authenticationModules&gt; Element (Network Settings)</span></span>
<span data-ttu-id="7d014-103">Spécifie les modules utilisés pour authentifier les demandes du réseau.</span><span class="sxs-lookup"><span data-stu-id="7d014-103">Specifies modules used to authenticate network requests.</span></span>  
  
 <span data-ttu-id="7d014-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="7d014-104">\<configuration></span></span>  
<span data-ttu-id="7d014-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="7d014-105">\<system.net></span></span>  
<span data-ttu-id="7d014-106">\<authenticationModules ></span><span class="sxs-lookup"><span data-stu-id="7d014-106">\<authenticationModules></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d014-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d014-107">Syntax</span></span>  
  
```xml  
<authenticationModules>   
</authenticationModules>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7d014-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7d014-108">Attributes and Elements</span></span>  
 <span data-ttu-id="7d014-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7d014-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7d014-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="7d014-110">Attributes</span></span>  
 <span data-ttu-id="7d014-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7d014-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="7d014-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7d014-112">Child Elements</span></span>  
  
|<span data-ttu-id="7d014-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7d014-113">**Element**</span></span>|<span data-ttu-id="7d014-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d014-114">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="7d014-115">add</span><span class="sxs-lookup"><span data-stu-id="7d014-115">add</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/add-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="7d014-116">Ajoute un module d’authentification à l’application.</span><span class="sxs-lookup"><span data-stu-id="7d014-116">Adds an authentication module to the application.</span></span>|  
|[<span data-ttu-id="7d014-117">clear</span><span class="sxs-lookup"><span data-stu-id="7d014-117">clear</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/clear-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="7d014-118">Efface tous les modules d’authentification de l’application.</span><span class="sxs-lookup"><span data-stu-id="7d014-118">Clears all authentication modules from the application.</span></span>|  
|[<span data-ttu-id="7d014-119">remove</span><span class="sxs-lookup"><span data-stu-id="7d014-119">remove</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/remove-element-for-authenticationmodules-network-settings.md)|<span data-ttu-id="7d014-120">Supprime un module d’authentification de l’application.</span><span class="sxs-lookup"><span data-stu-id="7d014-120">Removes an authentication module from the application.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7d014-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7d014-121">Parent Elements</span></span>  
  
|<span data-ttu-id="7d014-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7d014-122">**Element**</span></span>|<span data-ttu-id="7d014-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d014-123">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="7d014-124">System.NET</span><span class="sxs-lookup"><span data-stu-id="7d014-124">system.net</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="7d014-125">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="7d014-125">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7d014-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7d014-126">Remarks</span></span>  
 <span data-ttu-id="7d014-127">Le `authenticationModule` élément spécifie les modules d’authentification qui effectuent le processus d’authentification avec un serveur.</span><span class="sxs-lookup"><span data-stu-id="7d014-127">The `authenticationModule` element specifies the authentication modules that conduct the authentication process with a server.</span></span> <span data-ttu-id="7d014-128">Un module d’authentification doit implémenter le <xref:System.Net.IAuthenticationModule> interface.</span><span class="sxs-lookup"><span data-stu-id="7d014-128">An authentication module must implement the <xref:System.Net.IAuthenticationModule> interface.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="7d014-129">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="7d014-129">Configuration Files</span></span>  
 <span data-ttu-id="7d014-130">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="7d014-130">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d014-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d014-131">Example</span></span>  
 <span data-ttu-id="7d014-132">L’exemple suivant active un module d’authentification.</span><span class="sxs-lookup"><span data-stu-id="7d014-132">The following example enables an authentication module.</span></span> <span data-ttu-id="7d014-133">Vous devez remplacer les valeurs de Version et de PublicKeyToken par les valeurs correctes pour le module spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d014-133">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <add type="System.Net.DigestClient, System, Version=2.0.3600.0,  
                 Culture=neutral, PublicKeyToken=b77a5c561934e089" />  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7d014-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d014-134">See Also</span></span>  
 <xref:System.Net.IAuthenticationModule>  
 <xref:System.Net.AuthenticationManager>  
 [<span data-ttu-id="7d014-135">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="7d014-135">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
