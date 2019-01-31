---
title: <clear>, élément d'authenticationModules (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/authenticationModules/clear
- http://schemas.microsoft.com/.NetConfiguration/v2.0#clear
helpviewer_keywords:
- clear element, authenticationModules
- <authenticationModules>, clear element
- <clear> element, authenticationModules
- authenticationModules, clear element
ms.assetid: dc522c45-4a80-4831-8955-f7b68a47edfd
ms.openlocfilehash: d6760d05a8c2368cd20cae416b0b4b428b6588db
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55279069"
---
# <a name="clear-element-for-authenticationmodules-network-settings"></a><span data-ttu-id="64d11-102">\<Désactivez >, élément d’authenticationModules (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="64d11-102">\<clear> Element for authenticationModules (Network Settings)</span></span>
<span data-ttu-id="64d11-103">Efface tous les modules d’authentification à partir de l’application.</span><span class="sxs-lookup"><span data-stu-id="64d11-103">Clears all authentication modules from the application.</span></span>  
  
 <span data-ttu-id="64d11-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="64d11-104">\<configuration></span></span>  
<span data-ttu-id="64d11-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="64d11-105">\<system.net></span></span>  
<span data-ttu-id="64d11-106">\<authenticationModules></span><span class="sxs-lookup"><span data-stu-id="64d11-106">\<authenticationModules></span></span>  
<span data-ttu-id="64d11-107">\<clear></span><span class="sxs-lookup"><span data-stu-id="64d11-107">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64d11-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64d11-108">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="64d11-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="64d11-109">Attributes and Elements</span></span>  
 <span data-ttu-id="64d11-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="64d11-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="64d11-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="64d11-111">Attributes</span></span>  
 <span data-ttu-id="64d11-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="64d11-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="64d11-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="64d11-113">Child Elements</span></span>  
 <span data-ttu-id="64d11-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="64d11-114">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="64d11-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="64d11-115">Parent Elements</span></span>  
  
|<span data-ttu-id="64d11-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="64d11-116">**Element**</span></span>|<span data-ttu-id="64d11-117">**Description**</span><span class="sxs-lookup"><span data-stu-id="64d11-117">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="64d11-118">authenticationModules</span><span class="sxs-lookup"><span data-stu-id="64d11-118">authenticationModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/authenticationmodules-element-network-settings.md)|<span data-ttu-id="64d11-119">Spécifie les modules utilisés pour authentifier les demandes du réseau.</span><span class="sxs-lookup"><span data-stu-id="64d11-119">Specifies modules used to authenticate network requests.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64d11-120">Notes</span><span class="sxs-lookup"><span data-stu-id="64d11-120">Remarks</span></span>  
 <span data-ttu-id="64d11-121">Le `clear` élément supprime tous les modules d’authentification qui ont été définis précédemment dans le fichier de configuration ou à un niveau supérieur dans la hiérarchie de configuration.</span><span class="sxs-lookup"><span data-stu-id="64d11-121">The `clear` element removes all authentication modules that were defined earlier in the configuration file or at a higher level in the configuration hierarchy.</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="64d11-122">Fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="64d11-122">Configuration Files</span></span>  
 <span data-ttu-id="64d11-123">Cet élément peut être défini dans le fichier de configuration de l'application ou dans le fichier de configuration de l'ordinateur (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="64d11-123">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="64d11-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="64d11-124">Example</span></span>  
 <span data-ttu-id="64d11-125">L’exemple suivant supprime tous les modules d’authentification configuré.</span><span class="sxs-lookup"><span data-stu-id="64d11-125">The following example removes all configured authentication modules.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <authenticationModules>  
      <clear/>  
    </authenticationModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="64d11-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64d11-126">See also</span></span>
- <xref:System.Net.IAuthenticationModule>
- <xref:System.Net.AuthenticationManager>
- [<span data-ttu-id="64d11-127">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="64d11-127">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
